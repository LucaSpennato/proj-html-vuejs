<template>
  
    <footer>
        <LinksNavSection/>
        <FootBottomSection/>
    </footer>

</template>

<script>
import LinksNavSection from './FooterComponents/LinksNavSection.vue';
import FootBottomSection from './FooterComponents/FootBottomSection.vue';

export default {
    name: 'FooterComponent',
    components:{
        LinksNavSection,
        FootBottomSection,
    }
}
</script>

<style lang="scss">

</style>