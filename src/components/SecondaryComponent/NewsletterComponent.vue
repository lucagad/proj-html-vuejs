<template>
  <div class="container">
    <div class="background_img_container_right">
      <img class="d-none d-md-block img_top" src="../../assets/img/maxcoach-shape-08.png" alt="">
      <img class="d-none d-md-block img_bottom" src="../../assets/img/maxcoach-shape-02.png" alt="">
    </div>
    <div class="background_img_container_left">
      <img class="img_top" src="../../assets/img/maxcoach-shape-03.png" alt="">
    </div>
    <div class="text_box">
      <h2><bold>Subscribe</bold> <color>Newsletters</color></h2>
      <p>Enter your email address to register to our newsletter subscription <br> delivered on a regular basis!</p>
    </div>
    <div class="button_box">
      <input class="input_custom" type="search" placeholder="Enter your email" aria-label="Search">
      <a class="subscribe" href="#">Subscribe</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NewsletterComponent'

}
</script>

<style lang="scss" scoped>

@import '../../assets/style/general';
@import '../../assets/style/mixins';
@import '../../assets/style/utils';
@import '../../assets/style/vars';

.container{
  @include flex-column-cnt();
  margin-top: 40px;
  margin-bottom: 40px;
  position: relative;
  width: 100%;
  height: 300px;


  .background_img_container_left{
    position: absolute;
    left: 0;
    top: 140px;
    img{
      width: 90px;
    }
  }

  .background_img_container_right{
    position: absolute;
    right: 0;
    top: 100px;

    .img_bottom{
      position: relative;
    }

    .img_top{
      position: absolute;
      right: 0;
      top: -70px;
      transform: rotate(25deg);
    }

  }
}

.text_box{
  @include flex-column-cnt();
  text-align: center;

  color{
    color: $nl-title-text-color;
  }

  bold{
    font-weight: 900;
  }
}

.button_box{
  margin-top: 20px;
  @include flex-cnt();
  

  .input_custom{
    padding: 10px 60px 10px 20px;
    background-color: $input-background-color;
    font-size: 16px ;
    border: 1px solid $input-background-color;
    border-radius: 5px 0 0 5px;
  }
  
  .subscribe {
    margin-left: -5px;
    padding: 10px 20px;
    background-color: $nl-btn-background-color;
    border: 1px solid $input-background-color;
    border-radius: 0 5px 5px 0;

    text-decoration: none;
    color: $nl-btn-text-color;
    font-size: 16px ;
    font-weight: bold;
  }
}

</style>