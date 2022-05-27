<template>
  <footer class="wrapper">
    <div class="container footer_container">

      <div class="top_footer">
        <div class="col_left">
          <div class="address_box">
            <h5>Address</h5>
          </div>
        </div>
        <div class="col_right row">

          <div v-for="(element,index) in FooterElements" :key="`footer-element-${index}`" class="col_right_inside col">
            <h5>{{element.text}}</h5>

            <div class="list_elements">
              <ul>
                <li v-for="(link,index) in element.sublinks" :key="`footer-subelement-${index}`"><a :href="link.href">{{link.text}}</a></li>
              </ul>
            </div>

          </div>

        </div>
      </div>

      <div class="footer_bottom"> MAXCOACH</div>

    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent',
  props:{
    FooterElements: Array,
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/general';
@import '../assets/style/mixins';
@import '../assets/style/utils';
@import '../assets/style/vars';

.wrapper{
  position: relative;
  background-color: $footer-background-color;
  height: 400px;
  width: 100%;

  .footer_container{
    @include flex-column-cnt();
    color: $footer-text-color;

    .top_footer{
      margin-top: 80px;
      @include flex-sbtw();
      width: 100%;


      .col_right{ 
        width: 50%; 
        @include flex-sbtw();

        h5{ 
          color: $footer-title-color;
        }
        .col_right_inside{
          margin: 0 25px;
          width: 100%;

          .list_elements {
            width: 100%;
            ul {
              padding: 0;
              li { 
                list-style: none;
                margin-bottom: 10px;

                a{ 
                  text-decoration: none;
                  color: $footer-text-color;
                }
              }
            }
          }

        }
      }

      .col_left{
        width: 50%; 
        @include flex-sbtw();

        h5{ 
          color: $footer-title-color;
        }
      }
    }
  }

}

</style>