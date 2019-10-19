<template>
  <b-container fluid class="[ headerimage--container ]">
    <b-img
      fluid-grow
      class="[ article_headerImage ]"
      :src="articles.path"
      :alt="articles.alt"
      :title="articles.titlearrt"
    ></b-img>
    <b-container>
      <b-row>
        <b-col md="10" offset-md="1" class="[ articleHeader_container ]">
          <h2 class="[ articleHeader articleHeader_subHeader ]">{{ articles.category }}</h2>
          <h1 class="[ articleHeader articleHeader_headline ]">{{ articles.title }}</h1>
          <p class="[ articleHeader articleHeader_leadin ]">{{ articles.leadin }}</p>
          <b-img
            center
            width="20px"
            src="~/assets/images/angle-down-light.svg"
            class="[ articleHeader_caret ]"
          />
        </b-col>
      </b-row>
      <b-row>
        <b-col md="10" offset-md="1" class="[ articleBody_container ]">
          {{
          articles.bodyText
          }}
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
export default {
  name: 'ArticleItem',
  props: {
    path: String,
    title: String
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
.articleBody {
  font-family: $zenterfont;
  &_container {
    background-color: $white;
    padding-left: 180px;
    padding-right: 180px;
    padding-top: 40px;
    padding-bottom: 120px;
  }
  &_bodyHeadline {
    font-size: 24px;
    color: $primary;
    font-weight: 400;
  }
  &_bodyText {
    font-weight: 300;
    font-size: 16px;
    letter-spacing: 1px;
    &--italic {
      font-style: italic;
    }
  }
}

.information {
  &_container {
    border: 2px dashed $primary;
    background-color: rgba($primaryLight, 0.3);
    margin-top: 40px;
    padding: 20px;
  }
}
</style>
