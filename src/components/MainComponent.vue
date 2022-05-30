<template>
  <main>

    <CoursesComponent
    :CourseArray="this.OnlineCourses"/>

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


</style>