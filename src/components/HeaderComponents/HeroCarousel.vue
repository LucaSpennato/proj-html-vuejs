<template>
  <section class="carousel-section container-fluid p-0">
    <HeaderNav/>
    <div class="carousel text-center">
      ciao
    </div>
  </section>
</template>

<script>
import HeaderNav from './HeaderNav.vue';

export default {
    name: 'HeroCarousel',
    components:{
        HeaderNav,
    }
}
</script>

<style lang="scss">
    @import '../../scss/variables.scss';
    @import '../../scss/general.scss';
    @import '../../scss/containers.scss';
    .carousel-section{
      height: 100vh;
      // background-image: url('https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__480.jpg');
      background-image: url('../../assets/backgrounds/bg-parallax.png'), 
                        // carousel placeholder, the og one file is corrupted
                        url('https://static.vecteezy.com/system/resources/previews/006/304/593/original/abstract-white-and-light-grey-geometric-square-overlapped-pattern-on-background-with-shadow-modern-silver-color-cube-shape-with-copy-space-simple-and-minimal-banner-design-eps10-vector.jpg');
      background-position: center;
      // background-color: blue;
      .carousel{
        height: 90%;
      }

    }

</style>