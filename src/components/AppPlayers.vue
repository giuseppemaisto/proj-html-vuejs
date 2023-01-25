<template>
    <div class="contenitore">
        <div class="title">
        <h1>Our Team</h1>
        
        </div>
     
      <Carousel :items-to-show="4" :wrap-around="FALSE">
       
        <Slide v-for=" (item, index) in article" :key="index">
         
          <div class="slider">
  
              
              <img :src="item.image" />  
              <div class="info-player">
                <h5>{{ item.num }}</h5>
              <h2>{{ item.text }}</h2>
              </div>
            
              
              
          </div>
          
        </Slide>
    
        <template #addons>
          <Navigation />
        </template>
      </Carousel>

     </div> 
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
                      image:'/../public/img/player1.jpg',
                     num:'07',
                      text:'Adam Brown-forwarder'
                  },
                  {
                      image:'/../public/img/player2.jpg',
                      num:'11',
                      text:'Micheal Kayn-forwarder'
                   
                  },
                  {
                      image:'/../public/img/player3.jpg',
                      
                      num:'09',
                      text:'Micheal Lee-forwarder'
                  },
                    {
                      image:'/../public/img/player4.jpg',
                     
                      num:'15',
                      text:'Adam Brown-forwarder'
                  },
                
                  {
                      image:'/../public/img/player5.jpg',
                      
                      num:'09',
                      text:'Adam Brown-forwarder'
                  },
                  
              ]
          }
      },
     
    })
   
    </script>
    <style lang="scss" scoped>
.contenitore{
    background-image: url(../../public/img/player.jpg);
}

.title h2{
      text-align: center;
      font-size: 3px;
      
    }
    h1{
        text-align: center;
        font-weight: bold;
    }
  .slider{
      
      margin-bottom: 2rem;
   
      
      margin: 20px;

     img{
        width:300px;
        border-radius: 20px 20px 0 0 ;
     }
     
  
  
      
  
  
  }
  .info-player{
    width: 300px;
    border-radius:0 0 20px 20px;
    background-color:black ;   
     color:lightgrey
  }
  
  
  </style>