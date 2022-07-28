<template>
  
    <footer>
        <FooterLinksNavSection/>
        <FootBottomSection/>
    </footer>

</template>

<script>
import FooterLinksNavSection from './FooterComponents/FooterLinksNavSection.vue';
import FootBottomSection from './FooterComponents/FootBottomSection.vue';

export default {
    name: 'FooterComponent',
    components:{
        FooterLinksNavSection,
        FootBottomSection,
    }
}
</script>

<style lang="scss">

</style>