<template>
  <section id="about-company" class="container-fluid p-0">
        <div class="row col-12 m-0">
            <div class="col-6 d-flex justify-content-end mt-5 p-4">
                <div class="container-medium">
                    <div class="infos">
                        <h6 class="text-uppercase">
                            about the network
                        </h6>
                        <h1 class="fw-bold py-4">
                            <span>The</span>
                            Company
                        </h1>
                        <p>
                            For 12 years we have been rpviding audit and warranty, financial advice, risk advice, taxes and related services to select clients.
                        </p>
                    </div>
                    <div class="cards">
                        <div 
                        class="about-card" 
                        v-for="(card, index) in aboutTheCompanyInfos" :key="index">

                            <i :class="iconPath(card)"></i>
                            <h5>
                                {{ card.title }}
                            </h5>
                            <p>
                                {{ card.text }}
                            </p>

                        </div> 
                    </div>
                    <div>
                        <a class="btn" href="#">get in touch</a>
                        <a class="btn" href="#">read more</a>
                    </div>
                </div>
            </div>
            <div class="col-6 p-0">
                <img class="w-100" :src="require('../../assets/backgrounds/about-4.jpg')" alt="about-image">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AboutTheCompany',
    methods:{
        iconPath: function(object){
            return 'bi bi-' + object.icon;
        }
    },
    data: function(){
        return{
            aboutTheCompanyInfos:[
                {
                    icon: 'award',
                    title: 'tradition',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                },
                {
                    icon: 'lock',
                    title: 'security',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                },
                {
                    icon: 'pencil-square',
                    title: 'certificate',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                },
                {
                    icon: 'mortarboard',
                    title: 'expertise',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                },
            ]
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    #about-company{   
        background-color: $CcWoodsmoke;
        .infos{
            h1{
            color: white;
            }
            span{
                @include companyStyledWordBg;
            }
            h6{
                color: $CcBluelagoon;
            }
            p{
                color: $CcPumice;
            }
        }
        .about-card{
            display: inline-block;
            width: calc((100% / 2) - .6rem );
            margin-left: .3rem;
            margin-top: 1.7rem;
            i{
                color: $CcBluelagoon;
                font-size: 1.3rem;
            }
            h5{
                display: inline;
                color: $CcWhite;
                text-transform: capitalize;
                margin-left: .3rem;
            }
            p{
                margin-top: 1rem;
                color: $CcPumice;
            }

        }
        .container-medium a{
            @include inactiveElementGreen;

            &:hover{
                @include activeElementGreen;
            }
        }
    }
</style>