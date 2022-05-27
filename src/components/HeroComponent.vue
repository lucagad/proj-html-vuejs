<template>
  <div class="wrapper">

    <div class="hero_container">

        <div class="hero_text_box">

          <div class="pre_title">
            <span>Commerce Business</span>
          </div>

          <div class="title"> 
            <span>Distant Mentoring Program</span>
          </div>

        </div>

        <div class="hero_button_box"> 
            <button class="btn_hero">Download free guidebook <font-awesome-icon class="btn_arrow" icon="fa-solid fa-arrow-right" /></button>
        </div>

    </div>

    <div class="hero_right_bar">
      <a href="#"><font-awesome-icon class="hero_right_icon" icon="fa-solid fa-book-open" /></a>
      <a href="#"><font-awesome-icon class="hero_right_icon" icon="fa-solid fa-life-ring" /></a>
      <a href="#"><font-awesome-icon class="hero_right_icon" icon="fa-solid fa-book" /></a>
      <a href="#"><font-awesome-icon class="hero_right_icon" icon="fa-solid fa-cart-shopping" /></a>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HeroComponent'
}
</script>

<style lang="scss" scoped>

@import '../assets/style/general';
@import '../assets/style/mixins';
@import '../assets/style/utils';
@import '../assets/style/vars';

.wrapper{
  position: relative;
  background-image: url('../assets/img/home-3-hero-bg.jpg');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 600px;
  width: 100%;
  

  .hero_container{ 
    width: 50%;
    height: 100%;
    margin: 0 auto;
    @include flex-column-cnt();

    .hero_text_box{ 
      color: $hero-text-color;

      .pre_title{ 
        text-align: center;

        span{
          font-weight: bold;
          font-size: 1.5rem;
        }
      }

      .title{ 
        text-align: center;

        span{
          font-weight: 500;
          font-size: 3rem;
        }
      }

    }

    .hero_button_box{ 
      margin-top: 25px;

      .btn_hero{ 
        background-color: $hero-btn-background;
        
        padding: 15px 40px;
        border-radius: 10px;
        border: 1px solid $hero-btn-background;

        color: $hero-btn-text-color;
        font-weight: bold;

        &:hover{
          background-color: $hero-btn-text-color;
          border: 1px solid $hero-btn-text-color;

          color: $hero-btn-background;

        }

        .btn_arrow{ 
          margin-left: 10px;
        }
      }

    }
  }

  .hero_right_bar{ 
    position:absolute;
    top: 150px;
    right: 0;
    width: 50px;
    height: 200px;
    background-color: $hero-right-bar-background;
    border-radius: 5px 0 0 5px;

    @include flex-column-sbtw();

    .hero_right_icon{ 
      font-size: 20px;
      padding: 15px;
      color: $hero-right-bar-icon-color;
      cursor: pointer;
    }

  }

}


</style>