<template>
  <main>
    <div class="container_main">

      <div class="first_content">

        <div class="col_left">
          <div class="title_box">
            <span class="pretitle">EVERYTHING IN <bold>MAXCOACH</bold></span>
            <h2><bold>Learn about our </bold><br><color>Work Culture</color><bold> at <br>MaxCoach</bold></h2>
            <p>Spend some time to visit our website or head office and discover our current courses, enrollment procedure, and registration deadline. We're opening new classes every beginning of each month.</p>
            <span>Have questions?<a href="#"> Get Free Guide <font-awesome-icon class="btn_arrow" icon="fa-solid fa-arrow-right" /></a></span>
          </div>
        </div>

        <div class="col_right">
          
          <img class="img_back" src="../assets/img/stock-full-hd-10.jpg" alt="background image">
          
          <div class="overlay">
            <img class="img_top_left" src="../assets/img/maxcoach-shape-04.png" alt="shape">
            <img class="img_top" src="../assets/img/maxcoach-shape-07.png" alt="">
            <img class="img_top_woman" src="../assets/img/about-us-01.jpg" alt="woman">
            <img class="img_bottom" src="../assets/img/maxcoach-shape-02.png" alt="shape pixel">
          </div>
        </div>

      </div>

      <div class="second_content">
        <div class="first_box">
          <p class="box_number">129+</p>
          <p class="box_subtitle">Enrolled Learner</p>
        </div>
        <div class="second_box">
          <p class="box_number">80</p>
          <p class="box_subtitle">Finished Sessions</p>
        </div>
        <div class="third_box">
          <p class="box_number">4%</p>
          <p class="box_subtitle">Satisfaction Rate</p>
        </div>
      </div>

      <div class="third_content">

        <div class="col_left">
          <img class="img_back" src="../assets/img/stock-full-hd-11-670x450.jpg" alt="background youtube">
          <div class="overlay">
            <a href="#"><img class="img_youtube" src="../assets/img/icon-youtube-play.png" alt="youtube logo"></a>
          </div>
          
        </div>

        <div class="col_right">
          <div class="title_box">
            <span class="pretitle">How we work </span>
            <h2> <bold>Upgrade Your <br> Skills</bold> <color>Upgrade <br> Your Life</color></h2>
            <p>Opening up more opportunities in front of you to get the ticket to more enjoyable door in life. Getting equipped with new skills for new sets of insights into your career. MaxCoach accompany learners in every stage of learning.</p>
            <a href="#"> Download free guidebook <font-awesome-icon class="btn_arrow" icon="fa-solid fa-arrow-right" /></a>
          </div>
        </div>
      </div>

    </div>
    <CoursesComponent
    :CourseArray="this.OnlineCourses"/>

    <div class="container_main">

      <div class="fifth_content">

          <div class="col_left">
            <img class="img_back" src="../assets/img/home-3-team-image.png" alt="background team">
            <div class="overlay">
              <img class="img_bottom_right" src="../assets/img/maxcoach-shape-07-150x150.png" alt="Shape">
              <img class="img_top_left" src="../assets/img/maxcoach-shape-05-150x150.png" alt="Shape">
              <img class="img_bottom_left" src="../assets/img/maxcoach-shape-01.png" alt="Shape">
            </div>
            
          </div>

          <div class="col_right">
            <div class="title_box">
              <span class="pretitle">Everything in <bold>maxcoach</bold> </span>
              <h2> <bold>We're Here To <br></bold> <color>Trasform</color> <bold>You!</bold></h2>
              <p>As learners, people can enjoy great companionship from MaxCoach mentors and educators. We can help you develop and grow at your best.</p>
            <button class="btn_hero">Get Free Guide</button>

            </div>
          </div>
      </div>
  
    </div>

    <BlogComponent
    :BlogArray="this.BlogArticles"/>

    <NewsletterComponent />
    
  </main>
</template>

<script>
import BlogComponent from './SecondaryComponent/BlogComponent.vue'
import NewsletterComponent from './SecondaryComponent/NewsletterComponent.vue'
import CoursesComponent from './SecondaryComponent/CoursesComponent.vue'

export default {
  components: { NewsletterComponent, BlogComponent, CoursesComponent },
  name: 'MainComponent',
  props:{
    BlogArticles: Array,
    OnlineCourses: Array
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/general';
@import '../assets/style/mixins';
@import '../assets/style/utils';
@import '../assets/style/vars';

.container_main{
  width: 75%;
  height: 100%;
  margin: 0 auto;
}

.first_content{
  @include flex-cnt();
  margin-top: 120px;
  margin-bottom: 40px;
  
  .col_left{
    width: 40%;
    padding-left: 40px;

    .title_box{
      @include flex-column-start();
      color: $main-text-color;

      h2{
        margin: 20px 0;
        color: black;
      }

      a{
        color: $blog-title-text-color;
      }

      color{
        color: $blog-title-text-color;
        font-weight: lighter !important;
      }

      bold{
        font-weight: 900;
      }

      span{
        color: $blog-pretitle-text-color;
        font-size: 12px;

        &.pretitle{
          text-transform: uppercase;
        }
      }
    }
  }

  .col_right{
    @include flex-cnt();
    width: 60%;
    position: relative;
    

    .img_back{
      width: 500px;
      border-radius: 5px
    }

    .overlay{
      position: absolute;
    }

    .img_bottom{
      position: absolute;
      width: 80px;
      bottom: -205px;
      right: -195px;
      border-radius: 5px
    }

    .img_top{
      position: absolute;
      width: 80px;
      z-index: -1;
      top: -190px;
      right: -180px;
      border-radius: 5px
    }

    .img_top_left{
      position: absolute;
      width: 100px;
      top: -190px;
      right: 283px;
    }

    .img_top_woman{
      position: absolute;
      width: 135px;
      top: -225px;
      right: -275px;
      border-radius: 5px

    }
  }
}

.second_content{
  @include flex-cnt();
  text-align: center;
  margin-top: 70px;
  margin-bottom: 70px;

  .first_box,
  .second_box,
  .third_box{
    margin: 25px;
  }
  .box_number{
    font-size: 40px;
    color: $data-value-color;
    font-weight: bold; 
    margin-bottom: 0 !important; 
  }

  .box_subtitle{
    font-size: 12px;
    text-transform: uppercase;
    font-weight: bold; 
    color: $data-text-color;
  }

}

.third_content{
  @include flex-cnt();
  margin-top: 40px;
  margin-bottom: 40px;
  
  .col_right{
    width: 40%;
    padding-left: 25px;
    padding-right: 40px;

    .title_box{
      @include flex-column-start();
      color: $main-text-color;

      h2{
        margin: 20px 0;
        color: black;
      }

      a{
        color: $blog-title-text-color;
      }

      color{
        color: $blog-title-text-color;
        font-weight: lighter !important;
      }

      bold{
        font-weight: 900;
      }

      span{
        color: $blog-pretitle-text-color;
        font-size: 12px;

        &.pretitle{
          text-transform: uppercase;
        }
      }
    }
  }

  .col_left{
    @include flex-cnt();
    width: 60%;
    position: relative;
    
    .img_back{
      width: 600px;
      border-radius: 5px
    }

    .overlay{
      position: absolute;
    }
  }
}


.fifth_content{
  @include flex-cnt();
  margin-top: 120px;
  margin-bottom: 120px;
  
  .col_right{
    height: 100%;
    width: 40%;
    padding-left: 25px;
    padding-right: 40px;

    .title_box{
      @include flex-column-start();
      color: $main-text-color;

      h2{
        margin: 20px 0;
        color: black;
      }

      a{
        color: $blog-title-text-color;
      }

      color {
        color: $blog-title-text-color;
        font-weight: lighter !important;
      }

      bold{
        font-weight: 900;
      }

      span{
        color: $blog-pretitle-text-color;
        font-size: 12px;

        &.pretitle{
          text-transform: uppercase;
        }
      }
    }

    .btn_hero{ 
      background-color: $hero-btn-text-color;
      padding: 10px 40px;
      border-radius: 10px;
      border: 2px solid $hero-btn-text-color;

      color: $hero-btn-background;
      font-weight: bold;

      &:hover{
        background-color: $hero-btn-background;
        border: 2px solid $hero-btn-text-color;
        color: $hero-btn-text-color;

      }

      .btn_arrow{ 
        margin-left: 10px;
      }
    }
  }

  .col_left{
    @include flex-cnt();
    width: 60%;
    height: 100%;
    position: relative;
    
    .img_back{
      width: 600px;
      border-radius: 5px
    }

    .overlay{
      position: absolute;

      .img_bottom_right{
        position: absolute;
        width: 150px;
        bottom: -373px;
        right: -100px;
        z-index: -1;
      }

      .img_bottom_left{
        position: absolute;
        width: 150px;
        bottom: -180px;
        right: 375px;
      }

      .img_top_left{
        position: absolute;
        width: 150px;
        bottom: -40px;
        right: 220px;
        z-index: -1;
      }
    }
  }
}

</style>