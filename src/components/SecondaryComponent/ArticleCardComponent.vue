<template>
  <div class="container_article">
    <div class="image_box">
      <img :src="getImgUrl(ArticleData.img)" alt="">
    </div>
    <div class="text_box">
      <span class="article_author">{{ArticleData.author}}</span>
      <h5>{{ArticleData.title}}</h5>

      <div class="article_information">
        <div class="article_date">
          <font-awesome-icon icon="fa-regular fa-calendar" /> 
          <span>{{ArticleData.date}}</span>  
        </div>

        <div class="article_views">
          <font-awesome-icon icon="fa-regular fa-eye" />
          <span>{{ArticleData.views}} views</span> 
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'ArticleCardComponent',
  props:{
    ArticleData: Object
  },
  methods:{
    getImgUrl(pic){ return require('../../assets/img/'+ pic)}
  }


}
</script>

<style lang="scss" scoped>

@import '../../assets/style/general';
@import '../../assets/style/mixins';
@import '../../assets/style/utils';
@import '../../assets/style/vars';

.container_article{
  margin: 20px;
  height: 100%;
  width: 320px;
  padding-bottom: 30px;
  cursor: pointer;

  .image_box{
    width: 100%;
    border-radius: 5px;
    overflow: hidden;

    img{
      width: 100%;
    }
  }

  .text_box{
    width: 100%;
    margin-top: 20px;

    span{
      color: $article-text-color;
      font-size: 14px;

      &.article_author{
        text-transform: uppercase;
      }
    }
  
    .article_information{
      @include flex-start();

      .article_date,
      .article_views{
        color: $article-text-color;
        padding-right: 20px;

        span{
          padding-left: 10px ;
          font-size: 12px;
          line-height: 12px;
        }

      }
    }
  }
}

</style>