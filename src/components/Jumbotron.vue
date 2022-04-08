<template>
<div class="container-fluid">
    <ul id=menu>
        <li class="mb-3  bg-light"><a href="#"><img src="/images/svg-7.svg" alt="" class="img-fluid "></a></li>
        <li class="p-1 bg-light"><a href="#"><img src="/images/svg-6.svg" alt="" class="img-fluid "></a></li>
    </ul>
    <div class="row">
        <div class="col-4 p-0 position-relative hova-container" v-for="(img, index) in JumboList" :key="index ">
            <img :src="'./images/' + img.imgName" :alt="img.text" class="img-fluid">
            <div class="text ">
                The tiger is the largest cat species, reaching a
                total 
        </div>            
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
top: 10%;
width: 4em;
border: 2px solid magenta;
list-style-type: none;
z-index: 3;
}
.text{
position: absolute;
bottom: 30%;
left: 0;
background: black;
color: white;
margin-bottom: 5px;
font-family: sans-serif;
opacity: 0;
display: none;
-webkit-transition: visibility 0s, opacity 0.5s linear; 
transition: visibility 0s, opacity 0.5s linear;  
}
.hova-container:hover .text
    {
width: 150px;
padding: 8px 15px;
display:block;
opacity: 0.7;  
    }
</style>