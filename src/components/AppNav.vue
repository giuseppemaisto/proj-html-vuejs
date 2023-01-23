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
                <li v-for="(item, index) in Navbar" :key="index">
                    <a href="#">
                        {{item.label}}
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</template>
<style lang="">
    
</style>