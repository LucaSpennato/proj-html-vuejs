<template>       
    <ul id="nav-links" class="rounded">
        <li><h5>{{linksTitle}}</h5></li>
        <li v-for="(link, index) in links" :key="index">
            <span><i class="bi bi-chevron-right"></i></span>
            <a :href="link.url" @click.prevent>{{ link.text }}</a>
        </li>
    </ul>
</template>

<script>
export default {
    name: 'footerNav',
    props:{
        linksTitle: String,
        links: Array,
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    #nav-links{
        list-style: none;
        background-color: $secodaryDarkBrandBg;
        padding: 1.5rem;
        width: calc((100% / 4) - 2rem);

        li{
            color: $lightTextColor;
            text-transform: capitalize;

            a{
                font-size: .8rem;
                color: $secondaryTextColor;
                text-decoration: none;
            }
            i{
                margin-right: .3rem;
                font-size: .8rem;
            }
        }
    }

   
</style>