<template>
<header>
  <div class="container-fluid p-2">
    <div class="row justify-content-between">
      <div class="header-logo col-1">
        <img src="/images/logo-sidearea-1.png" alt="" class="my-logo-size">
        </div>
          <nav class="header-nav col-6">
            <ul class="d-flex justify-content-between fw-bold">
              <li v-for="(headerLink, index) in NavList" :key="index" @click="setActivePage(index)" :class="{ active: headerLink.current}">
                <a :href="headerLink.url" name="top">{{headerLink.link}}</a>
              </li>
              <li>
                <img src="/images/svg-1.svg" alt="" class="img-fluid">
              </li>          
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
        url : "#",
        current: true,
      },
      {
        link:"PAGES",
        url : "#",
        current: false,
      },
      {
        link:"PORTFOLIO",
        url : "#",
        current: false,
      },
      {
        link:"BLOG",
        url : "#",
        current: false,
      },
      {
        link:"SHOP",
        url : "#",
        current: false,
      },
      {
        link:"ELEMENTS",
        url : "#",
        current: false,
      },
      ],
    }
  },
  methods:{
        setActivePage(baseIndex){
            this.NavList.forEach((element, index) => {
                if (baseIndex === index ){
                    element.current = true;
                } else {
                    element.current = false;
                }
            });
      }}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
div.container-fluid{
  height: 50px;
}
.my-logo-size{
  width: 100px;
}
ul{
    list-style-type: none;
    height: 100%;
  }
  a{
    text-decoration: none;
    color: black;
}
ul li.active{
  border-bottom: 4px solid pink;
}

</style>
