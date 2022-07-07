<template>
  <div id="app">

    <PortfolioHeaderComponent />

    <HeaderComponent
    :HeaderElements="this.navbarItems" />

    <HeroComponent />

    <MainComponent
    :BlogArticles="this.blogArticles"
    :OnlineCourses="this.onlineCourses"/>

    <FooterComponent
    :FooterElements="this.footerItems"/>
    
  </div>
</template>

<script>

import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import MainComponent from './components/MainComponent.vue';
import HeroComponent from './components/HeroComponent.vue';
import PortfolioHeaderComponent from './components/PortfolioHeaderComponent.vue';

export default {
  name: "App",
  components: { HeaderComponent, FooterComponent, MainComponent, HeroComponent, PortfolioHeaderComponent },
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
      blogArticles:[
          {
            title: 'Brush Strokes Energize Trees in Paintings',
            author: 'Artist',
            img: 'artist-blog-03-480x325.jpeg',
            date: 'May 15, 2020',
            views: 688
          },
          {
            title: 'Pocket-Sized Notebooks Hold Miniature Paintings',
            author: 'Artist',
            img: 'artist-blog-01-480x325.jpg',
            date: 'May 15, 2020',
            views: 603
          },
          {
            title: 'Connection Between Self-Portraits and Identity',
            author: 'Artist',
            img: 'artist-blog-02-480x325.jpg',
            date: 'May 15, 2020',
            views: 397
          }
      ],
      onlineCourses:[
          {
            title: 'Learning to Write as a Professional Author',
            price: '40.00',
            img: 'course-02-480x298.jpg',
            lessons: 20,
            student: 50
          },
          {
            title: 'Customer-centric Info-Tech Strategies',
            price: '0.00',
            img: 'stock-full-hd-03-480x298.jpg',
            lessons: 24,
            student: 769
          },
          {
            title: 'Open Programming Courses for Everyone: Python',
            price: '19.00',
            img: 'stock-full-hd-04-480x298.jpg',
            lessons: 17,
            student: 62
          }
      ]

    }
  }
}
</script>

<style lang="scss">

@import './assets/style/general';
@import './assets/style/mixins';
@import './assets/style/utils';
@import './assets/style/vars';

</style>
