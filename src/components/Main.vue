<template>
  
  <main>
    <ServicesSection/>
    <AboutCompany/>
    <section>
        section two
    </section>

  </main>

</template>

<script>
import ServicesSection from './MainComponents/ServicesSection.vue';
import AboutCompany from './MainComponents/AboutCompany.vue';

export default {
    name: 'MainComponent',
    components:{
      ServicesSection,
      AboutCompany,
    }
}
</script>

<style lang="scss">

</style>