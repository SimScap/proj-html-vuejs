<template>
<div class="container-fluid">
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
                text:"First Jumbotron Pic",
            },
            {
                imgName:"h-2-port-img-2.jpg",
                text:"First Jumbotron Pic",
            },
            {
                imgName:"h-2-port-img-3.jpg",
                text:"First Jumbotron Pic",
                firstBug:"svg-6.svg",
                secondBug:"svg-7.svg",
            },
            {
                imgName:"h-2-port-img-4.jpg",
                text:"First Jumbotron Pic",
            },
            {
                imgName:"h-2-port-img-5.jpg",
                text:"First Jumbotron Pic",
            },
            {
                imgName:"h-2-port-img-6.jpg",
                text:"First Jumbotron Pic",
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
</style>