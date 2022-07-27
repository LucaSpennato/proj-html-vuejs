<template>
    <section id="action-projects" class="container-fluid flex-center">
        <div class="container-medium p-4">
            <div class="row text-center">

                <div class="col-12 infos">
                    <h6 class="text-uppercase">
                        we do more for everyone
                    </h6>
                    <h1 class="fw-bold py-4">
                        actions &
                        <span>projects</span>
                    </h1>
                </div>

                <div class="col-12 mb-5">
                    <nav>
                        <ul class="list-reset" v-for="(link, index) in navLinks" :key="index">
                            <li class="mx-1">
                                <a @click.prevent="navClick(index)" 
                                class="btn p-2" 
                                :class="{'active' : link.active}"
                                :href="link.url">{{ link.text }}</a>
                            </li>
                        </ul>
                    </nav>
                </div>

                <div class="col-12">
                    <div class="card-projects"
                    v-for="(card, index) in projectsInfos" :key="index">
                        <img class="img-fluid rounded" 
                        :src="imgPath(card)" 
                        :alt="imgPath(card) + 'project image'">
                        <p class="rounded">{{ card.text }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>

<script>
export default {
    name: 'ActionsAndProjects',
    methods:{
        navClick: function(index){
            this.navLinks.forEach(element => {
                element.active = false;
            });
            this.navLinks[index].active = true;
        },
        imgPath: function(object){
            return require('../../assets/projects/project-' + object.img + '.jpg');
        }
    },
    data: function(){
        return{
            navLinks:[
            {
                url: '#',
                text: 'all',
                active: true,
            },
            {
                url: '#',
                text: 'insitutional',
                active: false,
            },
            {
                url: '#',
                text: 'social',
                active: false,
            },
            {
                url: '#',
                text: 'events',
                active: false,
            },
            {
                url: '#',
                text: 'innovation',
                active: false,
            },
            {
                url: '#',
                text: 'enviroment',
                active: false,
            },
            {
                url: '#',
                text: 'technology',
                active: false,
            },
        ],
        projectsInfos:[
                {
                    img: '1',
                    text: 'Academic professional program in social media',
                },
                {
                    img: '2',
                    text: 'President\'s speech at the annual meeting',
                },
                {
                    img: '3',
                    text: 'International business trip in Shangai',
                },
                {
                    img: '4',
                    text: 'Technology workshop with educational theme',
                },
                {
                    img: '5',
                    text: 'Donation of clothes and food to the partner NGO',
                },
                {
                    img: '6',
                    text: 'Confraternization of the procurement team',
                },
            ] 
        }   
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';

    #action-projects{
        margin: 6rem 0;
        .infos{
            h1{
                text-transform: capitalize;
            }
            span{
                @include companyStyledWord;
            }
            h6{
                color: $CcBluelagoon;
                font-size: .8rem;
            }
            p{
                color: $CcPumice;
            }
        }

        nav{
        padding: 2rem 0;
        .active{
            background-color: rgba($CcBluelagoon, .3);
            border: 0;
        }
        ul li a{
            color: gray;
            text-transform: uppercase;
            a:hover{
                @include companyStyledWordBg;
                }
            }
        }
        .card-projects{
            display: inline-block;
            width: calc((100% / 3) - 1.6rem);
            margin: .8rem;
            position: relative;

            p{
                position: absolute;
                width: 100%;
                height: 100%;
                display: flex;
                align-items: flex-end;
                padding: 2rem 1rem;
                font-weight: bold;
                font-size: 1.2rem;
                color: $CcWhite;
                background-color: rgba(black, .4);
                top: 0;
            }
        }
    }

</style>