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
                <div class="col-12">
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
        navHover: function(){

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
        ] 
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';

    #action-projects{
        margin-top: 6rem;
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
        height: 3rem;
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