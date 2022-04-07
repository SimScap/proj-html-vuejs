<template>
  <div>
    <Header/>
    <Slide/>
    <Jumbotron/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Slide from './components/Slide.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'





export default {
  name: 'App',
  components: {
    Header,
    Slide,
    Jumbotron,
    Main,
    Footer,
  }
}
</script>

<style lang="scss">
@import '@/style/main-style.scss';
</style>
