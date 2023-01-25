<script>
    export default {
        data(){
            return{
                ArrayMatch:[
                    {
                        imgSquadra1:'/../public/img/club-3.png',
                        nameSquadra1:'Schalke Club',
                        nameSquadra2:'Inter Club',
                        imgSquadra2:'/../public/img/club-4.png',
                        data:'October 20, 2022 17:00 pm',
                        luogo:'Expert Stadium',
                    },
                    
                    {
                        imgSquadra1:'/../public/img/club-9.png',
                        nameSquadra1:'Atletico Club',
                        nameSquadra2:'Schalke Club',
                        imgSquadra2:'/../public/img/club-6.png',
                        data:'September 18, 2022 21:00pm',
                        luogo:'Expert Stadium',
                    },
                    
                    {
                        imgSquadra1:'/../public/img/club-2.png',
                        nameSquadra1:'United Fs Club',
                        nameSquadra2:'Bayern Club',
                        imgSquadra2:'/../public/img/club-8.png',
                        data:'August 3, 2022 19:00 pm',
                        luogo:'Expert Stadium'
                    },
                    {
                        imgSquadra1:'/../public/img/club-7.png',
                        nameSquadra1:'Arsenal Club',
                        nameSquadra2:'Atletico Club',
                        imgSquadra2:'/../public/img/club-9.png',
                        data:'July 8, 2022 12:00 pm',
                        luogo:'Expert Stadium',
                    },
                    {
                        imgSquadra1:'/../public/img/league-club-1.png',
                        nameSquadra1:'Instabul Sports',
                        nameSquadra2:'United Fs Club',
                        imgSquadra2:'/../public/img/club-2.png',
                        data:'june 12, 2022 09:00 am',
                        luogo:'Expert Stadium',
                    },
                ]
            }
        }
    }
</script>
<template lang="">
    <div class="contenitore">
        <ul class="d-flex">
            <li class="d-flex " v-for="(item, index) in ArrayMatch" :key="index">
              <div class="d-flex"> 
                <div class="nome">
                    <h2>{{item.nameSquadra1}}</h2>
                </div>
                <div class="squadre1">
                
                <img :src="item.imgSquadra1" alt="">
                 </div>
                 <h3 class="vs">VS</h3>
                <div class="squadre2">
                    <img :src="item.imgSquadra2" alt="">
                </div>
                <div class="nome">
                    <h2>{{item.nameSquadra2}}</h2>
                </div>
            </div>  
            <div class="luogo">
                <span>{{item.data}}</span>
                <span>{{ item.luogo}}</span>
            </div> 
           
             </li>
        </ul>
    </div>
</template>
<style lang="scss" scoped>

.contenitore{
    background-image: url(../../public/img/saha.jpg);
}
    ul{
        display: flex;
       flex-direction: column;
        justify-content: center;

        img{
            width:100px;
        }
        li{
            
            margin: 1rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            margin: auto;

            
        }
        .luogo{
            text-align: center;
            color: white;
            span{
                margin:1rem;
            }
        }
    }
    .squadre1{
        display: flex;
        flex-direction: column;
    }
    .nome{
        margin-top: 2rem;
        color:white
    }
    .vs{
        margin-top: 2rem;
        color:white
    }
</style>