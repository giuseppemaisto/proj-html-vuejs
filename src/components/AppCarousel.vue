        <script>
        export default {
            data(){
                return{
                        autoplay: null,
                        activeImage: 0,
                        slide:[
                                {
                                image: '/../public/img/slider1-1.jpg',
                                    
                                }, {
                                    image: '/../public/img/slider1-2.jpg',
                                    
                                }, {
                                    image: 'img/03.webp',
                                    title: 'Fortnite',
                                    text: "Grab all of your friends and drop into Epic Games Fortnite, a massive 100 - player face - off that combines looting, crafting, shootouts and chaos.",
                                }, {
                                    image: 'img/04.webp',
                                    title: 'Stray',
                                    text: 'Lost, injured and alone, a stray cat must untangle an ancient mystery to escape a long-forgotten city',
                                }, {
                                    image: 'img/05.webp',
                                    title: "Marvel's Avengers",
                                    text: 'Marvel\'s Avengers is an epic, third-person, action-adventure game that combines an original, cinematic story with single-player and co-operative gameplay.',
                                }
                        
                            ]
                    }  
            },
            methods: {
        changeSlide(index){
            this.activeImage=index;
        },
        next(){
            this.activeImage++
            if(this.activeImage >this.slide.length-1)
            this.activeImage = 0;
        },
        prev(){
            this.activeImage--;
            if(this.activeImage == 0){
                this.activeImage =this.slide.length-1
            }
        },
      
        stopAutoScroll(){
            clearInterval(this.autoplay);
            this.autoplay = null;
        }
    }
        }
        </script>
<template lang="">
    <div class="d-flex flex-column">
        <div class="container">
            
                <div class="item">
                    <div class="image" @mouseover="StopAutoScroll" @mouseleave="autoScroll">
                        <img :src="slide[activeImage].image" :alt="slide[activeImage].image">
                    </div>
                        <div class="text">
                            <h2>{{slide[activeImage].title}} </h2>
                            <p>{{slide[activeImage].text}}</p>
                        </div>
                </div>

               


        </div>
    </div>
</template>
<style lang="scss" scoped>

.image{
    height: 100%;
}
.item{
    float: left;
    width: 100%;
    height: 100%;
    position: relative;
    margin: none;
}
.item img {
width: 100%;
height: 100%;
object-fit: cover;
    
}

.item .text {
    position: absolute;
    right: 20px;
    bottom: 20px;
    text-align: right;
    color: white;
}







.prev, .next {
    width: 20px;
    height: 20px;
    
    border-radius: 50%;
    background: #ccc;
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    cursor: pointer;
    z-index: 999;
}

.next {
    bottom: 0;
}

/*
EXTRA: in questo esempio gli accordion vengono creati
usando 2 bordi di un quadratino ruotato di 45 gradi
In una versione base si possono usare delle icone
oppure i caratteri ∧ (&and;) e ∨ (&or;)
 */
.prev::after {
    content: '';
    width: 10px;
    height: 10px;
    border-top: 1px solid black;
    border-right: 1px solid black;
    display: block;
    position: absolute;
    top: 35%;
    left: 50%;
    transform: translate(-50%) rotate(-45deg);
}

.next::before {
    content: '';
    width: 10px;
    height: 10px;
    border-top: 1px solid black;
    border-right: 1px solid black;
    display: block;
    position: absolute;
    bottom: 35%;
    left: 50%;
    transform: translate(-50%) rotate(135deg);
}
</style>