<template>
  <section id="footer-top">
    <div class="container">
        <div class="row col-10">

            <LinksNav/>
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
                    about:[
                        {
                            url: '#',
                            text: '',
                        },
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
                    ],
                    Services:[
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
                    Support:[
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