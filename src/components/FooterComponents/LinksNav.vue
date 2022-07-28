<template>
    <ul id="nav-links" class="col-2 rounded mx-2">
        <li><h5>{{linksTitle}}</h5></li>
        <li v-for="(link, index) in links" :key="index">
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
        background-color: $MdBigStoneDarkVibrant;
        padding: 1.5rem;

        li{
            color: $CcWhite;
            text-transform: capitalize;

            a{
                color: $CcWhite;
                text-decoration: none;
            }
        }
    }

   
</style>