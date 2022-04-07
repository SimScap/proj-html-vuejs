<template>
<div class="container-fluid position-relative">
            <div id="" class="row text-center">
                <div class="col-12 p-3" id="my-before-carousel">
                </div>
                <div class="col-12">
                    <div class="my-carousel-container d-flex flex-column col-11 m-auto" id="my-carousel">
                        <div class="my-carousel-images d-flex justify-content-end">
                            <!-- immagini -->
                            <div class="carousel-text col-3 text-start">
                                <p>Devotion that never <span class="fw-bold">ends</span> </p>
                                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod Lorem ipsum dolor </p>
                                <button class="btn btn-light fw-bold">READ MORE</button>
                            </div>
                            <div class="item col-7" v-for="(element, index) in images" :key="index"
                                :class="(index == activeElement) ? 'active' : '' ">
                                <img class="img-fluid" :src="'./images/' + element.image" :alt="element.title">
                                <div class="item-description px-3">                            
                                </div>
                            </div>
                        </div>                      
                            <!-- prev -->
                            <div class="my-previous position-absolute">
                                <span class="my-prev-hook" @click="prevSlide()"></span>
                            </div>                         
                            <!-- next -->
                            <div class="my-next position-absolute">
                                <span class="my-next-hook" @click="nextSlide()"></span>
                            </div>
                        
                    </div>
                </div>
            </div>
        </div>
</template>

<script>
export default {
name: 'SlideContent',
data: function(){
    return{
        activeElement: 1,
        images: [{
            image:"h-2-slider-img-11.png"
        },
        {
            image:"h-2-slider-img-12.png"
        },
        {
            image:"h-2-slider-img-13.png"
        },
        {
            image:"h-2-slider-img-14.png"
        },
        {
            image:"h-2-slider-img-15.png"
        },
        {
            image:"h-2-slider-img-16.png"
        },
        {
            image:"h-2-slider-img-17.png"
        },
            
        ],
    }
},
methods: {
        nextSlide() {
            if (this.activeElement === this.images.length - 1) {
                this.activeElement = 0;
            } else {
                this.activeElement++;
            }
        },
        prevSlide() {
            if (this.activeElement === 0) {
                this.activeElement = this.images.length - 1;
            } else {
                this.activeElement--;
            }
        },
}}
</script>


<style scoped lang="scss">
body {
    font-family: "Montserrat", sans-serif;
}

div.my-carousel-container {
    border: 2px solid green;
}

div.my-previous,
div.my-next {
    height: 40px;
    width: 40px;
    border-radius: 50%;
    padding: 5px;
    background-color: rgba(255, 255, 255, .5);
    z-index: 1;
    top: 50%;
    transform: translateY(-50%);
    cursor: pointer;
    border: 2px solid black;
}

div.my-previous {
    left: .3rem;
}

div.my-next {
    right: .3rem;
}

div.my-previous>span::after {
    font-family: "Font Awesome 5 Free";
    font-weight: 900;
    content: "O";
    line-height: 30px;
}

div.my-next>span::after {
    font-family: "Font Awesome 5 Free";
    font-weight: 900;
    content: "O";
    line-height: 30px;
}


/* modifica css */

div.my-carousel-images .item {
    position: relative;
    display: none;
}


div.my-carousel-images .item.active {
    display: block;
}

div.my-carousel-images img {
    height: 100%;
    width: 100%;
    max-height: 350px;
    border: 2px solid gold;
}
div.carousel-text{
    border: 2px solid black;
}
button{
    border: 1px solid brown;
}
</style>
