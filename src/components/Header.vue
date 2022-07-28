<template>
  <header>
    <HeadTopSection/>
    <Hero/>
  </header>
</template>

<script>
import HeadTopSection from './HeaderComponents/HeadTopSection.vue';
import Hero from './HeaderComponents/Hero.vue';

export default {
    name: 'HeaderComponent',
    components:{
        HeadTopSection,
        Hero,
    }
}
</script>

<style lang="scss">
    

</style>