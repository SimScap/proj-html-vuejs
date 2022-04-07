<template>
<header>
  <div class="container-fluid">
    <div class="row justify-content-between">
      <div class="header-logo col-1">
        <img src="/images/logo-sidearea-1.png" alt="" class="img-fluid">
      </div>
      <nav class="header-nav col-6">
        <ul class="d-flex justify-content-between">
          <li v-for="(headerLink, index) in NavList" :key="index">{{headerLink.link}}</li>
          <img src="/images/svg-1.svg" alt="" class="img-fluid">
        </ul>
      </nav>
    </div>
  </div>
</header>
</template>

<script>
export default {
  name: 'HeaderContent',
  data: function(){
    return{
      NavList: [{
        link:"HOME",
      },
      {
        link:"PAGES",
      },
      {
        link:"PORTFOLIO",
      },
      {
        link:"BLOG",
      },
      {
        link:"SHOP",
      },
      {
        link:"ELEMENTS",
      },
      ],
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
div.container-fluid{
  height: 60px;
  div.header-logo{
    border: 2px solid black;

  }
  nav.header-nav{
    border: 2px solid green;
  }
  ul{
    list-style-type: none;
  }
}

</style>
