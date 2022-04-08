<template>
<div class="container-fluid">
    <div class="row">
        <div class="col-8 my-container m-auto text-center">
            <h4>Working Process</h4>
            <div class="process-container">
                <p>lorem</p>
            </div>
        </div>
        <div class="contact-content text-center">
            <div class="my-container col-6 m-auto">
                <h4>Want to work with us? Send us <span>a message!</span></h4>
                <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure perferendis culpa maxime eius itaque ducimus exercitationem natus nam quibusdam! Doloremque ipsum quis cumque velit, perferendis eaque et enim libero est!</p>
                <button class="custom-button">Contact</button>
            </div>         
        </div>
        <div class="event-content">

        </div>
    </div>
</div> 
</template>

<script>
export default {
    name: "MainContent",
    data: function(){
        return{
        eventList: [{
            img: "h-2-blog-img-1.jpg",
            text:"This way, loves: a detailed guide through new desing",
            author:"By Emily Fields",
        },
        {
            img: "h-2-blog-img-2.jpg",
            text:"I try to give people a different way of looking art",
            author:"By Emily Fields",
        },
        {
            img: "h-2-blog-img-3.jpg",
            text:"Introduce Richard Laperrière of those amazing features",
            author:"By Emily Fields",
        },
        ],
        }
    }
}
</script>

<style scoped lang="scss">
div.my-container{
    border: 2px solid black;
}
div.contact-content{
    border: 2px solid navy;
}
.custom-button{
    background-color:rgb(216, 240, 227) ;
    width: 150px;
}

</style>