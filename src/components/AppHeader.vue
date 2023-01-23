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
    <div>
        <AppNav :Navbar="Navbar"/>
    </div>
</template>
<style lang="">
    
</style>