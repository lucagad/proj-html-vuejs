<template>
  <div class="container navbar_container">
    <nav class="navbar_custom justify-content-md-between py-3 mb-4">

      <ul class="nav col-12 col-md-auto mb-2 justify-content-center mb-md-0">
        <li 
          v-for="(item,index) in HeaderElements" 
          :key="`header-${index}`" 
          class="dropdown">
          <a :href="item.href" class="nav-link dropdown_icon px-2 link-secondary">
            {{item.text}} 
            <font-awesome-icon icon="fa-solid fa-chevron-down" />
          </a>
        </li>
      </ul>

      <a href="/" class="logo col-md-3 mb-2 mb-md-0 text-dark text-decoration-none">
        <img src="../assets/img/dark-logo.png">
      </a>

      <div class="col_left col-md-3 text-end">
        <div class="cart">
          <a href="#">
            <font-awesome-icon icon="fa-solid fa-cart-shopping" />
            <div class="cart_number">0</div>
          </a>
        </div>
        <a><font-awesome-icon icon="fa-regular fa-circle-user" /></a>

        <div class="input_box">
          <input class="input_custom form-control me-2" type="search" placeholder="Search..." aria-label="Search">
          <font-awesome-icon class="icon_custom" icon="fa-solid fa-magnifying-glass" />
        </div>

      </div>

    </nav>
  </div>
</template>

<script>
export default {
  name: 'HeaderComponent',
  props:{
    HeaderElements: Array,
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/general';
@import '../assets/style/mixins';
@import '../assets/style/utils';
@import '../assets/style/vars';

.navbar_container{

  .navbar_custom{
    @include flex-cnt();
    color: $navbar-item-color;

    ul{
      li{
        a{ 
          color: $navbar-item-color;
          .fa-chevron-down{ 
            font-size: 10px 
          }
        }
      }
    }

    a.logo{
      @include flex-cnt();

      img{
      width: 180px;
      }

    }

    .col_left{
      @include flex-cnt();
      flex-wrap: nowrap;

      .cart{ 
        position: relative;
        padding: 10px;
        }

        .cart_number{ 
          position: absolute;
          right: 10px;
          top: 3px;
          width: 20px;
          height: 20px;
          border-radius: 50%;
          text-align: center;
          line-height: 20px;
          font-size: 15px;
          color: white;
          background-color: $cart-items-number;
      }

      a{
        font-size: 20px;
        margin: 15px;
        text-decoration: none;
        color: $navbar-item-color;
        cursor: pointer;
      }

      .input_box{
        position: relative;

        .icon_custom{ 
          position: absolute;
          top: 7px;
          right: 15px;
          color: $input-icon-color;
          cursor: pointer;
          
        }
      
        .input_custom{ 
          margin-left: 15px;
          background-color: $input-background-color;
          font-size: 12px ;
          border: 1px solid $input-background-color;
        }
      }
    }

  }
}


</style>