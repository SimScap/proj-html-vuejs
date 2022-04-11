<template>
<div class="container-fluid">
    <div class="row">
    <div class="col-12 my-container m-auto text-center p-5">
        <h4 class="fs-1">Working <span class="fst-italic fw-bold">Process</span> </h4>
        <div class="process-container d-flex m-auto col-10 justify-content-around">
            <div class="process-card align-self-end " v-for="(process, index) in processList" :key="index">
                <div class="process-card-logo d-flex justify-content-center m-auto mb-3">
                    <span class="align-self-center fs-1"><font-awesome-icon :icon="process.fontAwe" /></span>
                </div>
                    <h6 class="fw-bold">{{process.title}}</h6>
                    <p>{{process.text}}</p>
            </div>
            </div>
        </div>
        <div class="contact-content text-center">
            <div class="my-custom-container col-6 m-auto">
                <h4 class="mb-5">Want to work with us? Send us <span class="fst-italic fw-bold">a message!</span></h4>
                <p class="mb-5">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure perferendis culpa maxime eius itaque ducimus exercitationem natus nam quibusdam! Doloremque ipsum quis cumque velit, perferendis eaque et enim libero est!</p>
                <button class="custom-button">Contact</button>
            </div>                    
        </div>
        <div class="event-content col-10 m-auto d-flex justify-content-between">
        <div class="card p-3" v-for="(event, index) in eventList" :key="index" >
            <img :src="'./images/' + event.img" class="card-img-top">
            <div class="card-body">
            <h5 class="card-title">{{event.text}}</h5>
            <p class="card-text">{{event.author}}</p>
    </div>
</div>
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
        processList: [{
            fontAwe: "fa-solid fa-lightbulb",
            title: "First theres an idea",
            text: "Lorem ipsum sit conetu adipisc sed be et ore aligua pleasure itself",
        },
        {
            fontAwe: "fa-solid fa-comment",
            title: "Then we talk about",
            text: "Lorem ipsum sit conetu adipisc sed be et ore aligua pleasure itself",
        },
        {
            fontAwe: "fa-solid fa-cloud",
            title: "And we think about",
            text: "Lorem ipsum sit conetu adipisc sed be et ore aligua pleasure itself",
        },
        {
            fontAwe: "fa-solid fa-pen",
            title: "So we draw along",
            text: "Lorem ipsum sit conetu adipisc sed be et ore aligua pleasure itself",
        },
        ],
        }
    }
}
</script>

<style scoped lang="scss">
div.contact-content{
    background-image: url('../../public/images/h-2-background-1.jpg');
    background-size: cover;
    height: 330px;
    background-position: center;
}
.custom-button{
    background-color:rgb(216, 240, 227) ;
    width: 150px;
    align-self: center;
}
.custom-button:hover{
    background-color: rgb(225, 192, 176);
    transition: background-color 1s;
}
div.my-custom-container{
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
div.process-container{
    background-image: url('../../public/images/svg-3.svg');
    height: 350px;
    background-repeat: no-repeat;
    background-position: center;
    background-size: 75% ;
}
div.process-card{
width: 200px;
}
div.process-card-logo{
    background-color: rgb(250, 247, 242);
    height: 130px;
    border-radius: 50%;
    width: 130px;
}
.fa-lightbulb{
    color: rgb(186, 218, 201);
}
.fa-comment{
    color: rgb(249, 221, 93) ;
}
.fa-cloud{
    color: rgb(128, 70, 95);
}
.fa-pen{
    color: rgb(234, 90, 55);
}
.card{
    border: none;
}
</style>