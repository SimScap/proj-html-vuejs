<template>
<div class="container-fluid">
    <ul id=menu>
        <li class="mb-3 custom-icon text-white"><a><img src="/images/svg-7.svg" alt="" class="img-fluid "></a></li>
        <li class="p-1 bg-light"><a><img src="/images/svg-6.svg" alt="" class="img-fluid "></a></li>
    </ul>
    <ul id=toTheTopMenu>
        <li><a href="#top" class="text-white custom-awesome p-1">
                <font-awesome-icon :icon="['fas', 'arrow-up']" />
            </a>
        </li>
    </ul>
    <div class="row">
        <div class="col-4 p-0 position-relative hova-container" v-for="(img, index) in JumboList" :key="index ">
            <img :src="'./images/' + img.imgName" :alt="img.alt" class="img-fluid">
            <div class="text ">
                <h6 class="fw-bold">{{img.text}}</h6>
                <p>{{img.secondaryText}}</p>
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
                alt:"Jumbotron Pic",
                text:"All these illustrations",
                secondaryText: "Illustrations",
            },
            {
                imgName:"h-2-port-img-2.jpg",
                alt:"Jumbotron Pic",
                text:"Type and illustrations",
                secondaryText: "Illustrations",
            },
            {
                imgName:"h-2-port-img-3.jpg",
                alt:"Jumbotron Pic",
                text:"Draw and illustrate",
                secondaryText: "Illustrations",
            },
            {
                imgName:"h-2-port-img-4.jpg",
                alt:"Jumbotron Pic",
                text:"Illustrations of novels",
                secondaryText: "Illustrations",
            },
            {
                imgName:"h-2-port-img-5.jpg",
                alt:"Jumbotron Pic",
                text:"To many illustrations",
                secondaryText: "Illustrations",
            },
            {
                imgName:"h-2-port-img-6.jpg",
                alt:"Jumbotron Pic",
                text:"Dreams are illustrations",
                secondaryText: "Illustrations",
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
#toTheTopMenu,
#menu{
position: fixed;
right: 0;
width: 3.8em;
border: 2px solid magenta;
list-style-type: none;
z-index: 3;
}
#toTheTopMenu{
top: 97%;
}
#menu {
top: 10%;
}
.text{
position: absolute;
bottom: 30%;
left: 0;
background: white;
color: black;
opacity: 0;
display: none;
transition: 1ms;
-webkit-transition: visibility 0s, opacity 0.5s linear;  
}
.hova-container:hover .text
    {
width: 200px;
padding: 8px 15px;
display:block;
opacity: 1;  
    }
li.custom-icon{
    background: red;
    filter: brightness(8);
}
a.custom-awesome{
    background-color: rgb(192, 225, 207);
}
</style>