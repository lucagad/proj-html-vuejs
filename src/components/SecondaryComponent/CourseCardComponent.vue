<template>
  <div class="container_course">
    <div class="image_box">
      <img :src="getImgUrl(CourseData.img)" alt="">
      <img v-if="CourseData.price ==='0.00'" class="free_price" src="../../assets/img/free-label.png" alt="">
    </div>
    <div class="text_box">
      <span class="course_price">${{CourseData.price}}</span>
      <h5>{{CourseData.title}}</h5>

      <div class="course_information">
        <div class="course_lessons">
          <font-awesome-icon icon="fa-regular fa-file-lines" />
          <span>{{CourseData.lessons}} Lessons</span>  
        </div>

        <div class="course_students">
          <font-awesome-icon icon="fa-regular fa-user" />
          <span>{{CourseData.student}} Students</span> 
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'CourseCardComponent',
  props:{
    CourseData: Object
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

.container_course{
  margin: 20px;
  height: 100%;
  width: 320px;
  border-radius: 6px;
  background-color: $course-background-color;

  .image_box{
    position: relative;
    width: 100%;
    overflow: hidden;
    border-radius: 6px 6px 0 0;

    img{
      width: 100%;

      &.free_price{
        width: 55px;
        position: absolute;
        top: 5px;
        right: 5px;
      }
    }
  }

  .text_box{
    width: 100%;
    padding: 20px;

    span.course_price{
      text-transform: uppercase;
      color: $course-price-text-color;
      font-size: 20px;
      font-weight: bold;
    }
  }
  
    .course_information{
      @include flex-start();
      padding: 15px 0;

      .course_lessons,
      .course_students{
        color: $course-text-color;
        padding-right: 20px;

        span{
          padding-left: 10px ;
          font-size: 12px;
          line-height: 12px;
        }

      }
    }
}

</style>