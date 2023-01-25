<script>
export default {
    
}
</script>
<template lang="">
    <div class="container-match">
        <div class="squadra1 d-flex">
            <h3>instabul sports</h3>
            <img src="/../public/img/league-club-1.png" alt="">
        </div>
        <div class="vs">
            <h1>VS</h1>
        </div>
        <div class="squadra2 d-flex">
            <img src="/../public/img/club-2.png" alt="">
            <h3>United Fs Club</h3>
        </div>
    </div>

    <div class="info-match d-flex">
        <div>
            <h5><i class="fa-regular fa-calendar-days"></i> May 21, 2022 18:05 pm</h5>
        </div>
        <div>
            <h5><i class="fa-solid fa-circle-plus"></i> Expert Stadium</h5>
        </div>
    </div>

    <div class="button-match d-flex">
        <button>View Match Details</button>
    </div>
</template>

<style lang="scss">
.container-match{
    width: 100%;
    display: flex;
    justify-content: center;
}
.squadra1 h3{
    width: 250px;
    padding-top: 2rem;
    font-weight: bold;
}
.squadra2 h3{
    padding-top: 2rem;
    font-weight: bold;
}
.vs h1{
    padding-top:1rem;
    font-size:60px;
    font-weight: bold;
}
.info-match{
    justify-content: center;
    margin: 1rem
}
.info-match div{
    margin: 1rem;
}
.info-match h5{
    font-weight: bold;
}
.button-match{
    justify-content: center;
    padding: 1rem;
}
.button-match button{
  
    color:white;
    background-color: black;
    padding: 1rem 2rem 1rem 2rem;
    border-radius: 30px;
    font-weight: bold;
}

    
</style>