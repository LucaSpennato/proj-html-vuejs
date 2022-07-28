<template>
  <section id="footer-top">
    <div class="container">
        <div class="row col-10">
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
    data: function(){
        return{
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

</style>