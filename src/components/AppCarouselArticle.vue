<template>
    <Carousel :items-to-show="4" :wrap-around="true">

      <Slide v-for=" (item, index) in article" :key="index">
        <div class="slider">
            <img :src="item.image" />  
            <h5>{{ item.date }}</h5>
            <h2>{{ item.title }}</h2>
            <p>{{ item.text }}</p>
            <button>more</button>
        </div>
        
      </Slide>
  
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
  </template>
  
  <script>
  import { defineComponent } from 'vue'
  import { Carousel, Navigation, Slide } from 'vue3-carousel'
  
  import 'vue3-carousel/dist/carousel.css'
  
  export default defineComponent({
    name: 'WrapAround',
    components: {
      Carousel,
      Slide,
      Navigation,
    },
    data(){
        return {
            article:[
                {
                    image:'/../public/img/news1-1-223x223.png',
                    date:'29.05.2022- Football',
                    title:'What is Football?',
                    text:'Football is a sport that is known as a ball game and is loved by […]'
                },
                {
                    image:'/../public/img/news2-1-223x223.png',
                    date:'29.05.2022- Football',
                    title:'Football Features',
                    text:'Football; It is an aerobic-based anaerobic sport in which jumps, kicks, turns, running with changing […]'
                },
                {
                    image:'/../public/img/news3-1-223x223.png',
                    date:'29.05.2022- Football',
                    title:'Football reles',
                    text:'GOLDEN GOAL: In a football match, the goal scored by one of the teams in […]'
                },
                  {
                    image:'/../public/img/news4-1-223x223.png',
                    date:'29.05.2022- Football',
                    title:'Fotball Termes',
                    text:'GOLDEN GOAL: In a football match, the goal scored by one of the teams in […]'
                },
              
                {
                    image:'/../public/img/news6-1-223x223.png',
                    date:'29.05.2022- Football',
                    title:'Fotball Termes',
                    text:'GOLDEN GOAL: In a football match, the goal scored by one of the teams in […]'
                },
                
            ]
        }
    },
   
  })
 
  </script>
  <style lang="scss" scoped>
.slider{
    
    margin-bottom: 2rem;
    border:1px solid grey;
    border-radius: 20px;
    margin: 10px;
   


    button{
        background-color: black;
        color:white;
        padding: 0.5rem 2rem 0.5rem 2rem ;
        border-radius: 30px;
        margin-bottom: 1rem;
        font-weight: bold;
    }


}


</style>