<template>
  <section class="carousel-section container-fluid p-0">
    <HeaderNav/>
    <div class="carousel flex-center  text-center">
      <div class="container-small">
        <div class="display-1 fw-bold mb-4">
          {{ carouselElements[currentActive].title }}
        </div>
          <h5>
            {{ carouselElements[currentActive].description }}
          </h5>
        </div>
      </div>
      <div class="thumb-wrapper">
        <div class="lateral-thumb my-2"
        :class="{'active' : currentActive === index}" 
          v-for="(thumb, index) in carouselElements" :key="index">
            
        </div>
      </div>
  </section>
</template>

<script>
import HeaderNav from './HeaderNav.vue';

export default {
    name: 'HeroCarousel',
    components:{
        HeaderNav,
    },
    data: function(){
      return{
        currentActive: 1,
        carouselElements:[
          {
            title: 'example',
            description: 'No matter what your company needs, we will be ready to assist you in the best possible way',
            linkOne:{
              url: '#',
              text: 'get in touch',
            },
            linkTwo:{
              url: '#',
              text: 'read more',
            }
          },
          {
            title: 'ready team',
            description: 'No matter what your company needs, we will be ready to assist you in the best possible way',
            linkOne:{
              url: '#',
              text: 'get in touch',
            },
            linkTwo:{
              url: '#',
              text: 'read more',
            }
          },
          {
            title: 'example',
            description: 'No matter what your company needs, we will be ready to assist you in the best possible way',
            linkOne:{
              url: '#',
              text: 'get in touch',
            },
            linkTwo:{
              url: '#',
              text: 'read more',
            }
          },
        ]
      }
    }
}
</script>

<style lang="scss">
    @import '../../scss/variables.scss';
    @import '../../scss/general.scss';
    @import '../../scss/containers.scss';
    .carousel-section{
      height: 100vh;
      background-image: url('../../assets/backgrounds/bg-parallax.png'), 
                        // carousel placeholder, the og one file is corrupted
                        url('https://static.vecteezy.com/system/resources/previews/006/304/593/original/abstract-white-and-light-grey-geometric-square-overlapped-pattern-on-background-with-shadow-modern-silver-color-cube-shape-with-copy-space-simple-and-minimal-banner-design-eps10-vector.jpg');
      background-position: center;
      .carousel{
        height: 80%;
      };

      .thumb-wrapper{
        position: absolute;
        right: .8rem;
        top: 50%;

      }

      .lateral-thumb{
        height: 2.6rem;
        width: .7rem;
        border-radius: 20px;
        border: 2px solid $CcBluelagoon;
        

        &::after{
          content: '\00A0';
        }
      };

    }

</style>