        <script>
        export default {
            data(){
                return{
                        autoplay: null,
                        activeImage: 0,
                        slide:[
                                {
                                image: '/../public/img/slider1-1.jpg',
                                title: 'Welcome to',
                                text: 'Football Club',
                                secondText: 'Live Match fix types and results'
                                }, {
                                    image: '/../public/img/slider2-1.jpg',
                                    title: 'Football Club',
                                    text: 'Sport Club',
                                    secondText: 'private football Matches'
                                    
                                }, {
                                    image: '/../public/img/slider3.jpg',
                                    title: 'Professional Football',
                                    text: 'Football Club',
                                    secondText: 'football is the poetry to moviment'
                                   
                                }, {
                                    image: '/../public/img/slider4.jpg',
                                    title: 'Football Club',
                                    text: 'Sport Club',
                                    secondText: 'football is a head game'
                                    
                                }, 
                        
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
        startAutoplay(){
            this.autoplay = setInterval(() =>{
                this.next()
            }, 3000)
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
        
            
                <div class="item">
                    <div class="image" @mouseover="StopAutoScroll" @mouseleave="autoScroll">
                        <img :src="slide[activeImage].image" :alt="slide[activeImage].image">
                    </div>
                        <div class="text">
                            <h1>{{slide[activeImage].title}} </h1>
                            <h2>{{slide[activeImage].text}}</h2>
                            <h4>{{slide[activeImage].secondText}}</h4>
                        </div>
                </div>
                <div>
                    <div class="prev" @click="prev"></div>
                    <div class="next" @click="next"></div>
                </div>
                <div class="button">
                    <button>Learn More <i class="fa-solid fa-arrow-right"></i></button>
                </div>

               


        
    </div>
</template>
<style lang="scss" scoped>
 @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variable.scss' as *;

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
    right: 30%;
    bottom: 50%;
    text-align: center;
    color: white;
    
    

   
}
h1, h2{
    font-size: 6rem;
    font-weight: bold;
}
.button{
    position: absolute;
    top:100%;
    left: 45%;

    button{
        padding: 1rem;
        width: 150px;
        border-radius: 20px;
        border:1px solid white;
        background-color: transparent;
        color: white;
    }
}







.prev, .next {
    width: 20px;
    height: 20px;
    padding: 1rem;
    border-radius: 50%;
    background: rgba(204,204,204, 0.5);
    position: absolute;
    transform: translate(-100%);
    cursor: pointer;
    z-index: 999;
}
.prev{
    top: 70%;
    right: 90%;
    
}
.next{
right:2%;
top:70%
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