<template>
    <nav class="container-fluid flex-center">
        <div class="row container-medium">
            <div class="col-2 flex-center">
                <img class="w-75" :src="require('../../assets/logos/logo.png')" alt="">
            </div>
            <div class="col-10 text-end">
                <ul class="list-reset" v-for="(link, index) in navLinks" :key="index">
                    <li class="mx-2">
                        <a @click.prevent="navClick(index)" 
                        class="btn px-4 fw-semibold" 
                        :class="{'active' : link.active}"
                        :href="link.url">{{ link.text }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'HeaderNav',
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
                text: 'home',
                active: false,
            },
            {
                url: '#',
                text: 'services',
                active: false,
            },
            {
                url: '#',
                text: 'about',
                active: false,
            },
            {
                url: '#',
                text: 'projects',
                active: false,
            },
            {
                url: '#',
                text: 'results',
                active: false,
            },
            {
                url: '#',
                text: 'get in touch',
                active: true,
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

    nav{
        padding: 2rem 0;
        height: 3rem;
        ul li{
            text-transform: uppercase;
            a:hover{
                background-color: $CcBluelagoon !important;
                color: white !important;
            }
        }
    }
</style>