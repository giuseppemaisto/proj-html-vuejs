<script>
import AppCarousel from './AppCarousel.vue';
export default {
        components:{
            AppCarousel
        },
        data(){
            return{
                slider:[
                    {
                        image:'/../public/img/slider1-1.jpg'
                    },
                    {
                        image:'/../public/img/slider2-1.jpg'
                    },
                ]
            }
        }
}
</script>
<template lang="">
<AppCarousel></AppCarousel>
</template>
<style lang="scss" scoped>
*{
    
}

</style>