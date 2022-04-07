<template>
<header>
  <div class="container-fluid">
    <div class="row justify-content-between">
      <div class="header-logo col-1">
        <img src="" alt="">
      </div>
      <nav class="header-nav col-6"></nav>
    </div>
  </div>
</header>
</template>

<script>
export default {
  name: 'HeaderContent',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
div.container-fluid{
  height: 40px;
  div.header-logo{
    border: 2px solid black;
  }
  nav.header-nav{
    border: 2px solid green;
  }
}

</style>
