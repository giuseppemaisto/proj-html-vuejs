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
            <img class="sponsor" src="https://garantiwebtasarim.com/wordpress/footballclub/wp-content/uploads/2022/05/sponsor1.png" alt="">
            <img class="sponsor" src="https://garantiwebtasarim.com/wordpress/footballclub/wp-content/uploads/2022/05/sponsor2.png" alt="">
           <img src="https://garantiwebtasarim.com/wordpress/footballclub/wp-content/uploads/2022/05/logo-football.png" alt="logo">
            <div><font-awesome-icon icon="fa-brands fa-facebook-f" /></div>
            <span>SPONSOR</span>
          
        </div>
        <AppNav :Navbar="Navbar"/>
    </header>
</template>
<style lang="scss">
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variable.scss' as *;

    header{
        height: 200px;
        background-color: rgba(0,0,0,0.6);

        .logo{
            @include justify-content-center;
            color: white;
            span{
                margin: 1rem;
            }
        }
        .sponsor{
            height: 70px;
        }
    }
    
</style>