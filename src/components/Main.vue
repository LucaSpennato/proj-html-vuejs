<template>
  
  <main>
    <ServicesSection/>
    <AboutCompany/>
    <ActionsProjectsSection/>
    <OurNumbersSection/>
    <TechnologiesSection/>
    <GetInTouch/>
  </main>

</template>

<script>
import ServicesSection from './MainComponents/ServicesSection.vue';
import AboutCompany from './MainComponents/AboutCompany.vue';
import ActionsProjectsSection from './MainComponents/ActionsProjectsSection.vue';
import OurNumbersSection from './MainComponents/OurNumbersSection.vue';
import TechnologiesSection from './MainComponents/TechnologiesSection.vue';
import GetInTouch from './MainComponents/GetInTouch.vue';

export default {
    name: 'MainComponent',
    components:{
      ServicesSection,
      AboutCompany,
      ActionsProjectsSection,
      OurNumbersSection,
      TechnologiesSection,
      GetInTouch,
    }
}
</script>

<style lang="scss">

</style>