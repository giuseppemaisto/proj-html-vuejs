<script>
import AppCarousel from './AppCarousel.vue';
import AppMatch from './AppMatch.vue';
import AppSponsor from './AppSponsor.vue';
import AppCarouselArticle from './AppCarouselArticle.vue';

export default {
        components:{
            AppCarousel,
            AppMatch,
           AppSponsor,
            AppCarouselArticle,
           
        },
        data(){
            return{
                ArrayMatch:[
                    {
                        imgSquadra1:'/../public/img/club-3.png',
                        nameSquadra1:'Schalke Club',
                        nameSquadra2:'/../public/img/club-4.png',
                        imgSquadra2:'Inter Club',
                        data:'October 20, 2022 17:00 pm',
                        luogo:'Expert Stadium',
                    },
                    {
                        imgSquadra1:'/../public/img/club-9.png',
                        nameSquadra1:'Atletico Club',
                        nameSquadra2:'/../public/img/club-6.png',
                        imgSquadra2:'Schalke Club',
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
<AppCarousel></AppCarousel>
<AppMatch></AppMatch>
<AppSponsor></AppSponsor>
<AppCarouselArticle></AppCarouselArticle>
</template>
<style lang="scss" scoped>


</style>