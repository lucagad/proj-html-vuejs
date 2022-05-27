<template>
  <div id="app">

    <HeaderComponent
    :HeaderElements="this.navbarItems" />

    <HeroComponent />

    <MainComponent />
    <FooterComponent />
    
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import MainComponent from './components/MainComponent.vue';
import HeroComponent from './components/HeroComponent.vue';


export default {
    name: "App",
    components: { HeaderComponent, FooterComponent, MainComponent, HeroComponent },
    data(){
      return{

        navbarItems:[
          {
          text: 'Home',
          href: '#'
          },
          {
          text: 'Pages',
          href: '#'
          },
          {
          text: 'Courses',
          href: '#'
          },
          {
          text: 'Features',
          href: '#'
          },
          {
          text: 'Blog',
          href: '#'
          },
          {
          text: 'Shop',
          href: '#'
          },
        ],
        footerItems:[
          {
          text: 'Explore',
          sublinks:[ 
            {
            text: 'Start Here',
            href: '#'
            },
            {
              text: 'Blog',
              href: '#'
            },
            {
              text: 'About Us',
              href: '#'
            },
            {
              text: 'Success story',
              href: '#'
            },
            {
              text: 'Courses',
              href: '#'
            },
            {
              text: 'Contact Us',
              href: '#'
            }
          ]
          },
          {
          text: 'Information',
          sublinks:[ 
            {
            text: 'Membership',
            href: '#'
            },
            {
              text: 'Purchase guide',
              href: '#'
            },
            {
              text: 'Privacy policy',
              href: '#'
            },
            {
              text: 'Terms of service',
              href: '#'
            }
          ]
          },
        ],

      }
    },
    methods:{

    }
}
</script>

<style lang="scss">

@import './assets/style/general';
@import './assets/style/mixins';
@import './assets/style/utils';
@import './assets/style/vars';



</style>
