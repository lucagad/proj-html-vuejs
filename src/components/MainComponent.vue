<template>
  <main>
    <BlogComponent
    :BlogArray="this.BlogArticles"/>
    
    <NewsletterComponent />
  </main>
</template>

<script>
import BlogComponent from './SecondaryComponent/BlogComponent.vue'
import NewsletterComponent from './SecondaryComponent/NewsletterComponent.vue'

export default {
  components: { NewsletterComponent, BlogComponent },
  name: 'MainComponent',
  props:{
    BlogArticles: Array
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/general';
@import '../assets/style/mixins';
@import '../assets/style/utils';
@import '../assets/style/vars';


</style>