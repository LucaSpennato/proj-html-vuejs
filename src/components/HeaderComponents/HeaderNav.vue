<template>
        <nav>
            <div class="container">
                <div class="row col-10 offset-2">
                    <div class="col-2 flex-center">
                        <img class="w-75" :src="require('../../assets/logos/logo.png')" alt="">
                    </div>
                    <div class="col-8 text-end">
                        <ul class="list-reset" v-for="(link, index) in navLinks" :key="index">
                            <li class="mx-1">
                                <a @click.prevent="navClick(index)" 
                                class="btn p-2" 
                                :class="{'activeElementBrandColor' : link.active}"
                                :href="link.url">{{ link.text }}</a>
                            </li>
                        </ul>
                    </div>
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
    @import '../../scss/style.scss';

    nav{
        padding: 2rem 0;
        height: 3rem;
        ul li{
            text-transform: uppercase;
            a:hover{
                @include activeElementBrandColor;
            }
        }
    }
</style>