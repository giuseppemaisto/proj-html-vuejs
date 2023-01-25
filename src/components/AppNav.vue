        <script>
        export default {
            props:{
                Navbar: Array,
            }
        }
        </script>
<template lang="">
    <div>
        <nav class="navbar">
            <ul>
                <li class="list-header" v-for="(item, index) in Navbar" :key="index">
                    <a href="#">
                        {{item.label}}
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</template>
<style lang="scss">
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variable.scss' as *;

    ul{
        @include justify-content-center;
        margin: auto;  
        list-style: none;

        li a{
            padding: 1rem;
            list-style-type: none;
            text-decoration: none;
            font-size: 22px ;
            color:white;
            
            

        }

        .list-header:hover{
            border-bottom: 5px solid white;
        }
     }

</style>