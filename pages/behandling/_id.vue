<template>
  <div>
    <ArticleTemplate
      :id="card.id"
      :articleImage="card.articleImage"
      :articleSubHeader="card.articleSubHeader"
      :titleattr="card.titleattr"
      :articleTitle="card.articleTitle"
      :alt="card.alt"
      :articleBody="card.articleBody"
      :articleLeadin="card.articleLeadin"
    />
  </div>
</template>

<script>
import ArticleTemplate from '~/components/article/articleTemplate'
import treatmentCards from '../../constants/treatmentCards'

export default {
  validate({ params }) {
    return /^\d+$/.test(params.id)
  },
  asyncData({ route }) {
    const { id } = route.params
    const card = treatmentCards.find((card) => card.id === Number(id))
    return { card }
  },
  components: {
    ArticleTemplate
  },

  head() {
    return {
      title: `Zenter | ${this.card.articleTitle}`,
      meta: [
        {
          name: 'description',
          content: this.card.articleSubHeader
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
