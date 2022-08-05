<template>
  <section id="footer-top">
    <div class="container">
        <div class="row col-10 justify-content-around m-auto">
            <div class="col-3">
                <img class="w-50" :src="require('../../assets/logos/logo.png')" alt="brand-logo">
                <ul class="contact p-0">
                    <li>
                        a functional HTML template for corporate and business.
                    </li>
                    <li v-for="(contact, index) in contactUsInfo" :key="index">
                        <a :href="contact.url" @click.prevent>
                            <i :class="iconPath(contact)"></i>
                            <span>{{ contact.text }}</span>
                        </a>
                    </li>
                </ul>
                <a class="get-in-touch btn" href="#" @click.prevent>get in touch</a>
            </div>
            <LinksNavLists
            v-for="(lists, index) in footerLinks" :key="index"
            :linksTitle="lists.title"
            :links="lists.links"
            />
        </div>
    </div>

  </section>
</template>

<script>
import LinksNavLists from './LinksNavLists.vue';


export default {
    name:'FooterLinks',
    components:{
        LinksNavLists,
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
        background-color: $darkBrandBg;
            img{
                filter: hue-rotate(180deg) invert(100%);
            }
        .contact{
            list-style: none;
            margin: 1rem 0;
            li{
                text-transform: capitalize;
                margin-bottom: 1rem;
                color: $secondaryTextColor;
                font-size: .8rem;
            }
            a{
                color: $secondaryTextColor;
                text-decoration: none;
            }
            span{
                margin-left: .5rem;
                text-transform: capitalize;
            }
        }
        .get-in-touch{
                @include inactiveElementBrandColor;
                color: $CcWhite;
                margin-left: 0;

                &:hover{
                @include activeElementBrandColor;
            }
        }    
    }

</style>