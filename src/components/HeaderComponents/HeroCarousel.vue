<template>
  <section class="carousel-section p-0">
    <HeaderNav/>
    <div class="container">
      <div class="row carousel flex-center text-center">
        <div class="col-7" 
        @mouseover="heroAutoPlayStop()" @mouseleave="heroAutoplayStart()"
        v-for="(infos, index) in carouselElements" :key="index" 
        v-show="currentActive === index">
          <div class="title display-1 fw-bold mb-4">
            <span>
              {{ splitFirstTitleWord(infos.title)}}
            </span>
            <span>
              {{ splitSecondTitleWord(infos.title) }}
            </span>
          </div>
            <div class="decription fs-4 mb-4">
              {{ infos.description }}
          </div>
          <ul class="list-reset">
            <li>
              <a class="btn" :href="infos.linkGetInTouch.url">{{ infos.linkGetInTouch.text }}</a>
            </li>
            <li>
              <a class="btn" :href="infos.linkReadMore.url">{{ infos.linkReadMore.text }}</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="thumb-wrapper">
        <div class="lateral-thumb my-2"
        :class="{'activeGreenLink' : currentActive === index}" 
        @click="changeOnThumbClick(index)"
          v-for="(thumb, index) in carouselElements" :key="index">  
        </div>
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
    methods: {
      splitFirstTitleWord(element){
        let word = element.split(" ");
        return word[0]
      },
      splitSecondTitleWord(element){
        let word = element.split(" ");
        return word[1]
      },

      nextSlide: function(){
        if(this.currentActive === this.carouselElements.length -1){
              this.currentActive = 0;
            }else{
              this.currentActive++;
            }
      },

      heroAutoplayStart: function(){
        this.isHeroOn = setInterval(() => {
            this.nextSlide();
          },2000)
      },

      heroAutoPlayStop: function(){
        clearInterval(this.isHeroOn);
        this.isHeroOn = null;
      },

      changeOnThumbClick: function(index){
        this.currentActive = index;
        this.heroAutoPlayStop();
        setTimeout(() => {
          this.heroAutoplayStart();
        }, 5000);
      },
    },
    created(){
      this.heroAutoplayStart();
    },
    data: function(){
      return{
        currentActive: 1,
        isHeroOn: null,
        carouselElements:[
          {
            title: 'example 1',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ',
            linkGetInTouch:{
              url: '#',
              text: 'go to one',
            },
            linkReadMore:{
              url: '#',
              text: 'read more one',
            }
          },
          {
            title: 'ready team',
            description: 'No matter what your company needs, we will be ready to assist you in the best possible way',
            linkGetInTouch:{
              url: '#',
              text: 'get in touch',
            },
            linkReadMore:{
              url: '#',
              text: 'read more',
            }
          },
          {
            title: 'example 3',
            description: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam.',
            linkGetInTouch:{
              url: '#',
              text: 'go to three',
            },
            linkReadMore:{
              url: '#',
              text: 'read more three',
            }
          },
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
    @import '../../scss/style.scss';

    .carousel-section{
      background-image:
      url('../../assets/backgrounds/bg-parallax.png'),
      // carousel placeholder, the og one file is corrupted
      url('https://static.vecteezy.com/system/resources/previews/006/304/593/original/abstract-white-and-light-grey-geometric-square-overlapped-pattern-on-background-with-shadow-modern-silver-color-cube-shape-with-copy-space-simple-and-minimal-banner-design-eps10-vector.jpg');
      background-position:center;
      background-repeat: no-repeat;
      background-size: cover;

        .container{
          padding: 10rem 0;
          position: relative;
          display: flex;
          align-items: center;
          justify-content: center;          
          
          .title{
            text-transform: capitalize;

            span:last-child{
              @include companyStyledWord;
            }
          }

          .decription{
            color: darkgray;
          }

          ul li a{
            @include inactiveElementBrandColor;

            &:hover{
              @include activeElementBrandColor;
            }
          }
      }


      .thumb-wrapper{
        position: absolute;
        right: -2rem;
        top: 12rem;

      }

      .lateral-thumb{
        height: 2.6rem;
        width: .7rem;
        border-radius: 20px;
        border: 2px solid $CcBluelagoon;
        

        &::after{
          content: '\00A0';
        }
      }

    }

</style>