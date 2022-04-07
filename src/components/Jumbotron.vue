<template>
<div class="container-fluid">
    <div class="row">
        <div class="col-4 card" v-for="(img, index) in JumboList" :key="index">
            <img :src="'./images/' + img.imgName" alt="jumbopics">
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
                imgName:"h-2-port-img-1.jpg"
            },
            {
                imgName:"h-2-port-img-2.jpg"
            },
            {
                imgName:"h-2-port-img-3.jpg"
            },
            {
                imgName:"h-2-port-img-4.jpg"
            },
            {
                imgName:"h-2-port-img-5.jpg"
            },
            {
                imgName:"h-2-port-img-6.jpg"
            },
        ],
        }
    }
}
</script>

<style scoped lang="scss">
div.container-fluid{
    height: 400px;
    div.card{
        border: 2px solid black;
    }
}
.row{
    border: 2px solid purple;
}

</style>