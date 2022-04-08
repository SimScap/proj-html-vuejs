<template>
<div class="container-fluid">
    <div class="row">
    <div class="col-8 my-container m-auto text-center">
        <h4>Working Process</h4>
        <div class="process-container d-flex">
            <div class="process-card align-self-end " v-for="(process, index) in processList" :key="index">
                <div class="process-card-logo d-flex justify-content-center m-auto">
                    <span class="align-self-center fs-1"><font-awesome-icon :icon="process.fontAwe" /></span>
                </div>
                    <h6>{{process.title}}</h6>
                    <p>{{process.text}}</p>
            </div>
            </div>
        </div>
        <div class="contact-content text-center">
            <div class="my-custom-container col-6 m-auto">
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
        processList: [{
            fontAwe: "fa-solid fa-lightbulb",
            title: "First theres an idea",
            text: "Lorem ipsum sit conetu adipisc sed be et ore aligua pleasure itself",
        },
        {
            fontAwe: "...",
            title: "Then we talg about",
            text: "Lorem ipsum sit conetu adipisc sed be et ore aligua pleasure itself",
        },
        {
            fontAwe: "...",
            title: "And we think about",
            text: "Lorem ipsum sit conetu adipisc sed be et ore aligua pleasure itself",
        },
        {
            fontAwe: "...",
            title: "So we draw along",
            text: "Lorem ipsum sit conetu adipisc sed be et ore aligua pleasure itself",
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
    background-image: url('../../public/images/h-2-background-1.jpg');
    background-size: contain;
    height: 300px;
}
.custom-button{
    background-color:rgb(216, 240, 227) ;
    width: 150px;
    align-self: center;
}
div.my-custom-container{
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
div.process-container{
    background-image: url('../../public/images/svg-3.svg');
    height: 300px;
    background-repeat: no-repeat;
    background-position: center;
    background-size: 90%;
}
div.process-card{
border: 2px solid green;

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

</style>