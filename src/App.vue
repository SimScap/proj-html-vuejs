<template>
  <div>
    <Header/>
    <Slide/>
    <Jumbotron/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Slide from './components/Slide.vue'
import Jumbotron from './components/Jumbotron.vue'



export default {
  name: 'App',
  components: {
    Header,
    Slide,
    Jumbotron,
  }
}
</script>

<style lang="scss">
@import '@/style/main-style.scss';
</style>
