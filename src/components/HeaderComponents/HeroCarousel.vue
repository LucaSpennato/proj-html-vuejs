<template>
  <section class="carousel-section container-fluid p-0">
    <HeaderNav/>
    <div class="carousel flex-center  text-center">
      <div class="container-small">
        <div class="display-1 fw-bold mb-4">
        ready team
        </div>
          <h5>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis quas harum et, facilis obcaecati tempore aut facere, quis reiciendis inventore molestias exercitationem sed asperiores dolorum numquam fugit assumenda. Aliquam, sequi?
          </h5>
        </div>
      </div>
      <div class="lateral-thumb">
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

      .lateral-thumb::after{
        content: '\00A0';
        position: absolute;
        height: 2.6rem;
        width: .7rem;
        border-radius: 20px;
        border: 2px solid $CcBluelagoon;
        // background-color: red;
        right: .8rem;
        top: 50%;
      };

    }

</style>