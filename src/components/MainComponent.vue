<template>
  <main>
    <newsletter-component />
  </main>
</template>

<script>
import NewsletterComponent from './SecondaryComponent/NewsletterComponent.vue'
export default {
  components: { NewsletterComponent },
  name: 'MainComponent'
}
</script>

<style lang="scss" scoped>

@import '../assets/style/general';
@import '../assets/style/mixins';
@import '../assets/style/utils';
@import '../assets/style/vars';


</style>