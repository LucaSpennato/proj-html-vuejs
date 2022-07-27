<template>
  
  <main>
    <ServicesSection/>
    <AboutCompany/>
    <ActionsProjectsSection/>
    <OurNumbersSection/>
  </main>

</template>

<script>
import ServicesSection from './MainComponents/ServicesSection.vue';
import AboutCompany from './MainComponents/AboutCompany.vue';
import ActionsProjectsSection from './MainComponents/ActionsProjectsSection.vue';
import OurNumbersSection from './MainComponents/OurNumbersSection.vue';

export default {
    name: 'MainComponent',
    components:{
      ServicesSection,
      AboutCompany,
      ActionsProjectsSection,
      OurNumbersSection,
    }
}
</script>

<style lang="scss">

</style>