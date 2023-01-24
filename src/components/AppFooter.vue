<script>
import AppFooterInfo from './AppFooterInfo.vue';
export default {
    components: {
        AppFooterInfo
    },
        data(){
            return{
                menuFooter:[
                   {
                    label: 'Education',
                    details: [
                        'FIXTURES & RESULTS',
                        'LEAGUE TABLE',
                        'PLAYER',
                        'GALLERY',
                    ]
                   } ,
                   {
                    label: 'quick Links',
                    details: [
                        'HOME',
                        'BLOG',
                        'GALLERY',
                        'CONTACT',
                    ]
                   } ,
                ]
            }
        }
}
</script>
<template lang="">
<footer>
 
            <AppFooterInfo :menuFooter="menuFooter"/>

       
</footer>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variable.scss' as *;

    footer{
        background-color: black;
        height: 400px;
        color: white;
        padding: 1rem;

        .logo img{
            width: 60px;
            margin-left:4rem ;
            margin-bottom: 3rem;
            
        }

        ul{
            list-style-type: none;
            display: flex;
            flex-direction: column;

            li{
                margin: 0.5rem;
            }
        }
        .social{
            margin-left: 1rem;
            .icon{
                margin:  0 1rem 0 1rem;
                border: 1px solid white;
                padding: 0.5rem 1rem 0.5rem 1rem;
               
            }
        }

        .form-control{
            padding: 1rem;
            border-radius: 20px;
        }
        button{
            width: 500px;
            border-radius: 20px;
            padding: 1rem;
        }
    }
</style>