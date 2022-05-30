<template>
  <div class="wrapper">
    <div class="container">

      <div class="title_box">
        <span>Join Maxcoach at best</span>
        <h2><bold>Latest Online </bold> <color>Courses</color></h2>
      </div>

      <div class="courses_box">
        <CourseCardComponent 
        v-for="(course,index) in CourseArray" :key="`course-${index}`"
        :CourseData="course"/>

      <div class="slider">
        <div class="slider_slides">
          <div class="slider_slide"></div>
          <div class="slider_slide"></div>
          <div class="slider_slide"></div>
          <div class="slider_slide"></div>
          <div class="slider_slide"></div>
        </div>
        <div class="slider_dots">
          <a href="#" class="slider_indicator"></a>
          <a href="#" class="active slider_dot"></a>
          <a href="#" class="slider_dot" ></a>
          <a href="#" class="slider_dot" ></a>
          <a href="#" class="slider_dot" ></a>
          <a href="#" class="slider_dot" ></a>
        </div>
      </div>

      <div class="text_courses">
        <p>Control your personal preference settings to get notified about <br> appropriate courses. <a href="#"> View all courses <font-awesome-icon class="btn_arrow" icon="fa-solid fa-arrow-right" /></a></p>
      </div>
      
      </div>

    </div>
  </div>
</template>

<script>
import CourseCardComponent from './CourseCardComponent.vue'

export default {
  components: { CourseCardComponent },
  name: 'CoursesComponent',
  props:{
    CourseArray: Array
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

  .courses_box{
    @include flex-cnt-start();

    .slider {
      $dots: 5;
      $dotSize: .5;
      $dotMargin: .5;
	
      position: relative;
      width: 100%;
      height: 50px;
      overflow: hidden;
	
      .slider_slides {
        position: relative;
        width: $dots * 100%;
        height: 100%;
      }
	
      .slider_slide {
        float: left;
        width: 100% / $dots;
        height: 100%;
      }
	
      .slider_dots {
        display: flex;
        position: absolute;
        bottom: 1.5em;
        left: 50%;
        transform: translateX(-50%);
      }
	
      .slider_dot {
        display: block;
        margin: 0 #{ $dotMargin }em;
        width: #{ $dotSize }em;
        height: #{ $dotSize }em;
        background: #d8d8d8;
        border-radius: 100px;

        &.active{
          background: black;
          transform: scale(140%);
        }
      }
	
      .slider_indicator {
        @extend .slider_dot;
        position: absolute;
        background: black;
        width: auto;

      }
    }
  }

  .text_courses{
    text-align: center;
    font-size: 13px;
    color: $course-text-color;

    a{
      color: black;
      font-weight: bold;
    }
  }
}


</style>