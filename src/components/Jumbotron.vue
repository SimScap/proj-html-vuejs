<template>
<div class="container-fluid">
    <ul id=menu>
        <li><a href="#"><img src="/images/svg-7.svg" alt="" class="img-fluid bg-light"></a></li>
    </ul>
    <div class="row">
        <div class="col-4 p-0" v-for="(img, index) in JumboList" :key="index">
            <img :src="'./images/' + img.imgName" :alt="img.text" class="img-fluid">            
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: "JumbotronContent",
    data: function(){
        return{
            JumboList : [{
                imgName:"h-2-port-img-1.jpg",
                text:"Jumbotron Pic",
            },
            {
                imgName:"h-2-port-img-2.jpg",
                text:"Jumbotron Pic",
            },
            {
                imgName:"h-2-port-img-3.jpg",
                text:"Jumbotron Pic",
            },
            {
                imgName:"h-2-port-img-4.jpg",
                text:"Jumbotron Pic",
            },
            {
                imgName:"h-2-port-img-5.jpg",
                text:"Jumbotron Pic",
            },
            {
                imgName:"h-2-port-img-6.jpg",
                text:"Jumbotron Pic",
            },
        ],
        }
    }
}
</script>

<style scoped lang="scss">
.row{
    border: 2px solid purple;
}
#menu {
position: fixed;
right: 0;
top: 30%;
width: 4em;
border: 2px solid magenta;
list-style-type: none;
}
</style>