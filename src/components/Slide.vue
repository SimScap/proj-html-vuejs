<template>
<div class="container-fluid">
            <div id="app" class="row text-center">
                <div class="col-12 p-3" id="my-before-carousel">
                </div>
                <div class="col-12 p-5">
                    <div class="my-carousel-container d-flex flex-column px-5" id="my-carousel">
                        <div class="my-carousel-images">
                            <!-- immagini -->
                            <div class="item" v-for="(element, index) in images" :key="index"
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
    min-height: 700px;
    min-width: 800px;
}

div.my-thumbnails {
    background-color: violet;
    min-height: 160px;
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
}

div.my-previous {
    left: 1rem;
}

div.my-next {
    right: 1rem;
}

div.my-previous>span::after {
    font-family: "Font Awesome 5 Free";
    font-weight: 900;
    content: "\f7fb";
    line-height: 30px;
}

div.my-next>span::after {
    font-family: "Font Awesome 5 Free";
    font-weight: 900;
    content: "\f520";
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
    max-height: 500px;
}

div.my-carousel-images .item-description {
    position: absolute;
    bottom: 1rem;
    right: 1rem;
    color: white;
    text-align: end;
}

div .my-thumbnails {
    display: flex;
    overflow-y: auto;
}

div.thumbnail {
    flex-basis: 20%;
    filter: brightness(.4);
}

div.thumbnail img {
    height: 100%;
    width: 100%;
}

div.my-thumbnails .thumbnail.active {
    filter: brightness(1);
    border: 3px rgb(197, 197, 197) solid;
}

</style>
