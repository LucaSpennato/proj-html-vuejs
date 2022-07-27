<template>
  
  <main>
    <ServicesSection/>
    <AboutCompany/>
    <ActionsProjectsSection/>
  </main>

</template>

<script>
import ServicesSection from './MainComponents/ServicesSection.vue';
import AboutCompany from './MainComponents/AboutCompany.vue';
import ActionsProjectsSection from './MainComponents/ActionsProjectsSection.vue';

export default {
    name: 'MainComponent',
    components:{
      ServicesSection,
      AboutCompany,
      ActionsProjectsSection,
    }
}
</script>

<style lang="scss">

</style>