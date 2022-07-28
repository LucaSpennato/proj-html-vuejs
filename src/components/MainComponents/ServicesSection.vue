<template>
  <section id="services" class="container-fluid">
    <div class="container">
        <div class="row col-10 offset-1">
            <div class="row justify-content-center mb-4">
                <div class="infos col-8 px-4">
                    <h6 class="text-uppercase">
                        our business areas
                    </h6>
                    <h1 class="fw-bold py-4">
                        Exellence in <span>Services</span>
                    </h1>
                    <p>
                        We are leaders in providing consultancy with a set of cutting-edge technologies and a team of experienced and renowed professionals. These are some options that you can hire.
                    </p>
                </div>
                <div class="col-2 d-flex align-items-end justify-content-end">
                    <a class="text-uppercase btn activeGreenLink px-4 mb-4" @click.prevent href="#">see all</a>
                </div>
            </div>
            <div class="row gap-3 justify-content-center">
                <div
                v-for="(card, index) in servicesInfos" :key="index" 
                class="col-3 services-card rounded">
                    <div>
                        <div class="d-flex justify-content-between">
                            <i :class="iconPath(card)"></i>
                            <a :href="card.url" @click.prevent>
                                <i class="bi bi-arrow-right-short"></i>
                            </a>
                        </div>
                        <h5>{{ card.title }}</h5>
                        <p class="card-text">{{ card.text }}</p>
                    </div>
                </div>
            </div>    
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: 'ServicesSection',
    methods:{
        iconPath: function(object){
            return 'bi bi-' + object.icon;
        }
    },
    data: function(){
        return{
            servicesInfos:[
                {
                    icon: 'hdd-network',
                    title: 'audit & assurance',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'briefcase',
                    title: 'financial advisory',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'bar-chart',
                    title: 'analitics and m&a',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'airplane',
                    title: 'middle marketing',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'globe',
                    title: 'legal consulting',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'inbox',
                    title: 'regulatory risk',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
            ]
            
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    #services{
        background-color: $ServicesBg;
        padding: 8rem 0;
        .infos{
            span{
                @include companyStyledWord;
            }
            h6{
                color: $CcBluelagoon;
                font-size: .8rem;
            }
            p{
                color: gray;
            }
        }

        .services-card{
            padding: 1.8rem;
            background-color: $CcWhite;

            i{
                font-size: 2rem;
                color: $CcBluelagoon;
            }

            h5{
                text-transform: capitalize;
                padding: 1.2rem 0;
            }

            a{
                display: none;
                opacity: .6;
            }

            &:hover a{
                display: inline-block;
            }

        }
    }

</style>