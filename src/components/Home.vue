<template>
  <div>
    <app-intro/>
    <app-collaborate-partners/>
    <app-machinery/>
    <app-product-carousel/>
    <app-slogan/>
  </div>
</template>

<script>
  import Intro from './commons/Intro';
  import CollaboratePartners from './commons/CollaboratePartners';
  import Machinery from './commons/Machinery';
  import Slogan from './commons/Slogan';
  import ProductCarousel from './commons/ProductCarousel';

  export default {
    components: {
      'app-intro': Intro,
      'app-collaborate-partners': CollaboratePartners,
      'app-machinery': Machinery,
      'app-slogan': Slogan,
      'app-product-carousel': ProductCarousel,
    },
    created(){
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    },
  }
</script>

<style scoped>
</style>
