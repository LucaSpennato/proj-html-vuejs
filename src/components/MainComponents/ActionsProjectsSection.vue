<template>
    <section id="action-projects" class="container">
        <div class="p-4 flex-center">
            <div class="row col-10 text-center">
                
                <SectionsHeadings :info="titleInfo" />

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

                <ProjectsCards v-for="(projCard, index) in projectsInfos" :key="index" :card="projCard"/>

            </div>
        </div>
    </section>

</template>

<script>
import SectionsHeadings from './SectionsHeadings.vue';
import ProjectsCards from './ProjectsCards.vue';

export default {
    name: 'ActionsAndProjects',
    components:{
        SectionsHeadings,
        ProjectsCards,
    },
    methods:{
        navClick: function(index){
            this.navLinks.forEach(element => {
                element.active = false;
            });
            this.navLinks[index].active = true;
        },
    },
    data: function(){
        return{
            titleInfo:{
                topSubtitle: 'we do more for everyone',
                title: 'actions & projects',
                description: false,
                typeOne: true,
                typeTwo: false,
            },
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
        margin: 6rem auto;

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
    }

</style>