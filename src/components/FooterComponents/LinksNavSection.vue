<template>
  <section id="footer-top">
    <div class="container">
        <div class="row col-10">
            <div class="col-5">
                <ul class="contact" >
                    <li v-for="(contact, index) in contactUsInfo" :key="index">
                        <a :href="contact.url" @click.prevent>
                            <i :class="iconPath(contact)"></i>
                            <span>{{ contact.text }}</span>
                        </a>
                    </li>
                </ul>
            </div>
            <LinksNav
            v-for="(lists, index) in footerLinks" :key="index"
            :linksTitle="lists.title"
            :links="lists.links"
            />
        </div>
    </div>

  </section>
</template>

<script>
import LinksNav from './LinksNav.vue';

export default {
    name:'FooterLinks',
    components:{
        LinksNav,
    },
    methods:{
        iconPath: function(object){
            return 'bi bi-' + object.icon + '-fill';  
        }
    },
    data: function(){
        return{
            contactUsInfo: [
                {
                    icon: 'telephone',
                    url: '#',
                    text: '+1(305) 1234-5678',
                },
                {
                    icon: 'envelope',
                    url: '#',
                    text: 'hello@example.com',
                },
                {
                    icon: 'geo-alt',
                    url: '#',
                    text: 'main avenue, 987',
                },
            ],
            footerLinks:[
                {
                    title:'about',
                    links:[
                        {
                            url: '#',
                            text: 'the company',
                        },
                        {
                            url: '#',
                            text: 'institutional',
                        },
                        {
                            url: '#',
                            text: 'social & events',
                        },
                        {
                            url: '#',
                            text: 'innovation',
                        },
                        {
                            url: '#',
                            text: 'environment',
                        },
                        {
                            url: '#',
                            text: 'technology',
                        },
                    ],
                },
                {
                    title:'services',
                    links:[
                        {
                            url: '#',
                            text: 'audit & assurance',
                        },
                        {
                            url: '#',
                            text: 'financial advisory',
                        },
                        {
                            url: '#',
                            text: 'analitics M&A',
                        },
                        {
                            url: '#',
                            text: 'middle marketing',
                        },
                        {
                            url: '#',
                            text: 'legal consulting',
                        },
                        {
                            url: '#',
                            text: 'regulatory risk',
                        },
                    ],
                },
                {
                    title:'support',
                    links:[
                        {
                            url: '#',
                            text: 'responsability',
                        },
                        {
                            url: '#',
                            text: 'terms of use',
                        },
                        {
                            url: '#',
                            text: 'about cookies',
                        },
                        {
                            url: '#',
                            text: 'privacy policy',
                        },
                        {
                            url: '#',
                            text: 'accessibility',
                        },
                        {
                            url: '#',
                            text: 'information',
                        },
                    ]
                },
            ]
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    #footer-top{
        padding: 7rem;
        background-color: $CcWoodsmoke;
        .contact{
            list-style: none;
            margin: 1rem 0;
            li{
                margin: 1rem 0;
            }
            a{
                color: $CcPumice;
                text-decoration: none;
            }
            span{
                margin-left: .5rem;
                text-transform: capitalize;
            }
        }

    }

</style>