<template>
  <div id="app">
    <Header/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  }
}
</script>

<style lang="scss">
  @import '~bootstrap/scss/bootstrap.scss';
  @import '~bootstrap-icons/font/bootstrap-icons.css';
  @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Montserrat:ital,wght@0,100;0,300;0,400;0,500;0,700;0,800;1,200;1,700;1,800&display=swap');

  #app{
    font-family: 'Bebas Neue', cursive;
    font-family: 'Montserrat', sans-serif;
  }

</style>
