<template>
  <div id="app">
    <!-- All this webpage is not created on a Responsive design -->
    <Header />
    <Main />
    <Footer />
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
@import "./style/variables.scss";
@import "./style/general.scss";


#app {
  font-family: 'K2D', sans-serif; ;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: $darkBlueBg;
}

</style>
