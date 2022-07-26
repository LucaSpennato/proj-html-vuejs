<template>
  <header>
    <HeadTopSection/>
    <HeroCarousel/>
  </header>
</template>

<script>
import HeadTopSection from './HeaderComponents/HeadTopSection.vue';
import HeroCarousel from './HeaderComponents/HeroCarousel.vue';

export default {
    name: 'HeaderComponent',
    components:{
        HeadTopSection,
        HeroCarousel,
    }
}
</script>

<style lang="scss">
    

</style>