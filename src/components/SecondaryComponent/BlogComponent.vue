<template>
  <div class="wrapper">
    <div class="container">

      <div class="title_box">
        <span>Read for More joyment</span>
        <h2><bold>Latest From </bold> <color>Our Blogs</color></h2>
      </div>

      <div class="article_box">
        <ArticleCardComponent 
        v-for="(article,index) in BlogArray" :key="`blog-article${index}`"
        :ArticleData="article"/>
      </div>

    </div>
  </div>
</template>

<script>
import ArticleCardComponent from './ArticleCardComponent.vue'
export default {
  components: { ArticleCardComponent },
  name: 'BlogComponent',
  props:{
    BlogArray: Array
  }

}
</script>

<style lang="scss" scoped>

@import '../../assets/style/general';
@import '../../assets/style/mixins';
@import '../../assets/style/utils';
@import '../../assets/style/vars';


.wrapper{
  background-color: $blog-background-color;
}

.container{
  @include flex-column-cnt();
  padding-top: 75px;
  padding-bottom: 50px;

  .title_box{
    text-align: center;

    h2{
      margin: 20px 0;
    }

    color{
      color: $blog-title-text-color;
      font-weight: 300 !important;
    }

    bold{
      font-weight: 900;
    }

    span{
      text-transform: uppercase;
      color: $blog-pretitle-text-color;
      font-size: 12px;
    }
  }

  .article_box{
    @include flex-cnt-start();

  }
}


</style>