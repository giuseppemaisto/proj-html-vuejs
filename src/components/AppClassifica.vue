<script>
export default {
    data(){
        return{
            table:[
                {
                    image:'/../public/img/club-1.png',
                    nameteam:'Instabul Sports',
                    win:'18',
                    draw:'2',
                    lose:'0',
                    points:'42,',
                },
                {
                    image:'/../public/img/club-2.png',
                    nameteam:'United',
                    win:'14',
                    draw:'2',
                    lose:'1',
                    points:'35',
                },
                {
                    image:'/../public/img/club-3.png',
                    nameteam:'Shalke',
                    win:'13',
                    draw:'3',
                    lose:'0',
                    points:'32',
                },
                {
                    image:'/../public/img/club-4.png',
                    nameteam:'inter club',
                    win:'13',
                    draw:'2',
                    lose:'1',
                    points:'31',
                },
                {
                    image:'/../public/img/club-6.png',
                    nameteam:'United',
                    win:'12',
                    draw:'1',
                    lose:'2',
                    points:'30',
                },
                {
                    image:'/../public/img/club-7.png',
                    nameteam:'Madrid',
                    win:'11',
                    draw:'0',
                    lose:'3',
                    points:'28',
                },
                {
                    image:'/../public/img/club-8.png',
                    nameteam:'United',
                    win:'14',
                    draw:'2',
                    lose:'1',
                    points:'35',
                },
                {
                    image:'/../public/img/club-9.png',
                    nameteam:'United',
                    win:'14',
                    draw:'2',
                    lose:'1',
                    points:'35',
                },
                {
                    image:'/../public/img/club-11.png',
                    nameteam:'United',
                    win:'14',
                    draw:'2',
                    lose:'1',
                    points:'35',
                },
            ]
        }
    }
}
</script>
<template lang="">
    <div>
        <div class="classifica">
            <div class=" class-title d-flex ">
                <div>team</div>
                <div>W</div>
                <div>D</div>
                <div>L</div>
                <div>Pts</div>
            </div>
            <ul>
                <li class="d-flex" v-for="(item, index ) in table" :key="index">
                <div class=" class d-flex flex-direction-row">
                <div><img :src="item.image" alt=""></div>
                <div><h6>{{item.nameteam}}</h6></div>
                <div><h6>{{item.win}}</h6></div>
                <div><h6>{{item.draw}}</h6></div>
                <div><h6>{{item.lose}}</h6></div>
                <div class="punti"><h5>{{item.points}}</h5></div>
            </div> 
                </li>
             

            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    ul{
        display: flex;
        flex-direction: column;

        li{
            display: flex;
            flex-direction:row;

            img{
                width: 40px;
            }
        }

        .class{
          border:1px solid black;
            background-color: lightgrey;
        }
        .class div{
            width: 100px;
            padding: 1rem;
            margin: 0.5rem;
            
        }
    }
    .class-title{
        margin-left: 2rem;
        width: 700px;
        background-color: black;
    }
    .class-title div{
        width: 100px;
            justify-content: space-around;
            margin-left:7rem;
            color:white
    }
    .punti{
        
    }
</style>