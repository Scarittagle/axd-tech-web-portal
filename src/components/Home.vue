<template>
  <div>
    <app-intro/>
    <app-collaborate-partners/>
    <app-machinery/>
    <div
      style="background-color:#20314c"
      class="columns is-vcentered is-marginless">
      <div class="column is-paddingless">
        <div
          class="has-text-centered">
          <h1 class="title is-size-1 carousel-title">合作产品展示</h1>
          <h2 class="subtitle carousel-subtitle">Collaborate Product Showcase</h2>
        </div>
      </div>
      <div class="column is-paddingless">
        <app-product-carousel/>
      </div>
    </div>
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
  .carousel-title {
    color: white;
  }
  .carousel-subtitle {
    color: white;
    font-family: 'Questrial', sans-serif;
  }
</style>
