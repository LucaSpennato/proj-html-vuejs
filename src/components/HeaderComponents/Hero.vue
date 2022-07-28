<template>
  <section id="hero-section" class="p-0">
    <HeaderNav/>
    <Carousel/>
  </section>
</template>

<script>
import HeaderNav from './HeaderNav.vue';
import Carousel from './Carousel.vue';

export default {
    name: 'Hero',
    components:{
        HeaderNav,
        Carousel,
    },

}
</script>

<style lang="scss" scoped>
    @import '../../scss/style.scss';

    #hero-section{
      background-image:
      // carousel placeholder, the og one file is corrupted
      url('https://static.vecteezy.com/system/resources/previews/006/304/593/original/abstract-white-and-light-grey-geometric-square-overlapped-pattern-on-background-with-shadow-modern-silver-color-cube-shape-with-copy-space-simple-and-minimal-banner-design-eps10-vector.jpg');
      background-position:center;
      background-repeat: no-repeat;
      background-size: cover;
    }

</style>