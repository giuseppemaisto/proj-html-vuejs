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
                    label: 'EDUCATION',
                    details: [
                        'FIXTURES & RESULTS',
                        'LEAGUE TABLE',
                        'PLAYER',
                        'GALLERY'
                    ]
                   } ,
                   {
                    label: 'quick Links',
                    details: [
                        'HOME',
                        'BLOG',
                        'GALLERY',
                        'CONTACT'
                    ]
                   } ,
                ]
            }
        }
}
</script>
<template lang="">
<footer>
    <div class="row">
        <div class="col">
            <div class="logo">
                logo
            </div>
            <div class="contatti">
                <div>contatti</div>
                <div>contatti</div>
                <div>contatti</div>
            </div>
            <div class="social"></div>

        </div>
        <div class="col">
            <div class="newsletter">
                <div class="newsletter-text"></div>
                <div class="input-mail"></div>
            </div>
        </div>
        <div class="col">

            <AppFooterInfo :menuFooter="menuFooter"/>

        </div>
    </div>
</footer>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variable.scss' as *;

    footer{
        background-color: black;
        height: 300px;
        color: white;
    }
</style>