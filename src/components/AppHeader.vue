 <script>
    import AppNav from './AppNav.vue';
    export default {
        components:{
            AppNav
        },
            data(){
                return{
                    Navbar:[
                        {
                            label: 'HOME',
                        },
                        {
                            label: 'FIXTURES & RESULS'
                        },
                        {
                            label: 'LEAGUE TABLE'
                        },
                        {
                            label: 'PLAYERS'
                        },
                        {
                            label:'GALLERY',

                        },
                        {
                            label:'BLOG'

                        },
                        {
                            label:'CONTACT'
                        },
                    ]
                }
            }
    }
 </script>
<template lang="">
    <header>
        <div class="logo">
            <img class="sponsor" src="/../public/img/sponsor1.png" alt="">
            <img class="sponsor" src="/../public/img/sponsor2.png" alt="">
           <img src="/../public/img/favicon-football.png" alt="logo">
           <a ><i class="fa-brands fa-facebook-f fa-2x mx-2"></i></a>
            <a><i class="fa-brands fa-instagram fa-2x mx-2"></i></a>
            <i class="fa-brands fa-twitter fa-2x mx-2"></i>

        </div>
        <AppNav :Navbar="Navbar"/>
    </header>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variable.scss' as *;

    header{
        height: 200px;
        background-color: rgba(0,0,0,1);
     

        .logo{
            @include justify-content-center;
            color: white;
            margin-bottom: 3rem;
           
           
        }
        .sponsor{
            height: 70px;
        }

        
    }
    
</style>