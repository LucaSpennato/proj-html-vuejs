<template>
  <div class="container">
      <div id="carousel" class="row flex-center text-center">
        <div class="col-7" 
        @mouseover="heroAutoPlayStop()" @mouseleave="heroAutoplayStart()"
        v-for="(infos, index) in carouselElements" :key="index" 
        v-show="currentActive === index">
          <div class="title display-2 fw-bold mb-4">
            <span>
              {{ splitTitleWord(infos.title, 0)}}
            </span>
            <span>
              {{ splitTitleWord(infos.title, 1) }}
            </span>
          </div>
            <div class="description mb-4">
              {{ infos.description }}
          </div>
          <ul class="list-reset-inline">
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
        :class="{'activeElementBrandColor' : currentActive === index}" 
        @click="changeOnThumbClick(index)"
          v-for="(thumb, index) in carouselElements" :key="index">  
        </div>
      </div>
    </div>
</template>

<script>
export default {
    name: 'Carousel',
    data: function(){
      return{
        currentActive: 1,
        isHeroOn: null,
        carouselElements:[
          {
            title: 'example 1',
            description: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam.',
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
    },
      methods:{
      splitTitleWord(element, wordIndex){
        let word = element.split(" ");
        return word[wordIndex]
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
          this.heroAutoPlayStop();
          this.heroAutoplayStart();
        }, 5000);
      },
    },
    created(){
      this.heroAutoplayStart();
    },
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
        
        .container{
            position: relative;
        }
          #carousel{
            background-image: url('../../assets/backgrounds/bg-parallax.png');
            background-position: center;
            background-size: 200%;
            background-repeat: no-repeat;
            padding: 10rem 0;
            display: flex;
            align-items: center;
            justify-content: center;          
            
            .title{
                text-transform: capitalize;
                span:last-child{
                @include companyStyledWord;
                }
            }

            .description{
              margin: 0 auto;
              display: flex;
              align-items: center;
              width: 60%;
              height: 5rem;
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
            right: -5%;
            top: 50%;
            transform: translate(-50%, -50%);
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

</style>