<template>
  <b-container fluid class="[ headerimage--container ]">
    <b-img
      fluid-grow
      class="[ article_headerImage ]"
      :src="articleImage"
      :alt="alt"
      :title="titleattr"
    ></b-img>
    <b-container>
      <b-row>
        <b-col md="10" offset-md="1" class="[ articleHeader_container ]">
          <h2 class="[ articleHeader articleHeader_subHeader ]">{{ articleSubHeader }}</h2>
          <h1 class="[ articleHeader articleHeader_headline ]">{{ articleTitle }}</h1>
          <p class="[ articleHeader articleHeader_leadin ]">{{ articleLeadin }}</p>
          <b-img
            center
            width="20px"
            src="~/assets/images/angle-down-light.svg"
            class="[ articleHeader_caret ]"
          />
        </b-col>
      </b-row>
      <b-row>
        <b-col md="10" offset-md="1" class="[ articleBody_container ]" v-html="articleBody"></b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
export default {
  name: 'ArticleTemplate',
  props: {
    articleImage: String,
    articleTitle: String,
    articleLeadin: String,
    articleBody: String,
    articleSubHeader: String,
    titleattr: String,
    alt: String
  }
}
</script>

<style lang="scss" scoped>
.headerimage--container {
  padding: 0px !important;
}
.article {
  &_headerImage {
    position: fixed;
    top: -80px;
    bottom: -80px;
    z-index: -100;
  }
}
.articleHeader {
  font-family: $zenterfont;
  letter-spacing: 0.8px;
  &_container {
    background-color: rgba($secondaryDark, 0.8);
    padding: 40px;
    padding-bottom: 20px;
    color: $white;
    margin-top: 34%;
    border-radius: 10px 10px 0 0;
  }
  &_subHeader {
    color: $primary;
    text-transform: uppercase;
    font-size: 24px;
  }
  &_headline {
    font-size: 60px;
    font-weight: 600;
  }
  &_leadin {
    font-size: 18px;
    padding-top: 15px;
  }
  &_caret {
    padding-top: -20px;
  }
}
</style>
