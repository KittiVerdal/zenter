<template>
  <div>
    <ArticleTemplate :path="card.path" :alt="card.alt" />
  </div>
</template>

<script>
import ArticleTemplate from '~/components/article/articleTemplate'
import injuryCards from '../../constants/injuryCards'

export default {
    validate ({ params }) {
        return /^\d+$/.test(params.id)
    },
    asyncData({ route }) {
        const { id } = route.params
        const card = injuryCards.find(card => card.id === Number(id))
        return { card }
    },
    components: {
        ArticleTemplate
    },

  head() {
    return {
      title: 'title on Plager page comes here',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'page description is written in more detail here for SEO'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.header_headline--blue {
  color: $primaryLight;
}
.cards {
  &--marginTop {
    margin-top: 40px;
  }
}
</style>
