<template>
  <div>
    <Header/>
    <Slide/>
    <Jumbotron/>
    <Main/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Slide from './components/Slide.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'




export default {
  name: 'App',
  components: {
    Header,
    Slide,
    Jumbotron,
    Main,
  }
}
</script>

<style lang="scss">
@import '@/style/main-style.scss';
@import '@/fortawesome/fontawesome-free/css/all.min.css';
</style>
