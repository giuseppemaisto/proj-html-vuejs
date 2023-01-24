        <script>
        export default {
            props: {
                menuFooter: Array
            }
        }
        </script>
<template lang="">
     <div class="row d-flex">
                 <div class="col">
                    <div class="logo">
                        <img  src="/../public/img/logo-footer-football.png" alt="logo-footer">
                    </div>
                    <div class="contatti">

                        <ul class="list-contatti">

                            <li><i class="fa-solid fa-location-dot"></i>  New Jersey, USA</li>
                            <li><i class="fa-solid fa-phone-volume"></i> +1(234)567 89 10</li>
                            <li><i class="fa-solid fa-envelope"></i>example@example.com</li>
                        </ul>
                    </div>
                    <div class="social d-flex">
                        <div class="icon"><i class="fa-brands fa-facebook-f fa-2x"></i></div>
                        <div class="icon"><i class="fa-brands fa-instagram fa-2x"></i></div>
                        <div class="icon"><i class="fa-brands fa-twitter fa-2x"></i></div>
                    </div>

                </div>
                <div class="col">
                    <div class="newsletter my-4">
                        <div class="newsletter-text">
                            <h2>Join Our Newsletter</h2>
                            <p>Subscibe to be informed about important developments in our club and football world</p>
                        </div>
                        <div class="input-mail">
                            <div class="mb-3">
                            
                            <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="Your Email Address">
                            </div>
                            <button type="button" class="btn btn-light">Subscribe <i class="fa-solid fa-arrow-right"></i></button>
                        </div>
                    </div>
                </div>
                <div class="col d-flex my-4">

                    <ul class="list-footer d-flex ">
                        <li v-for="(item, index) in menuFooter" :key="index">
                            
                            <h2> {{item.label}} </h2> 
                                
                        
                            
                            <li class=" item my-2" v-for="(item, index) in item.details" :key="index"><a href="#"><span>{{ item }}</span></a></li>
                            
                            
                        </li>
                    </ul>
            
                    

                </div>
    </div>

    <div class="copyright d-flex justify-content-center my-4">
        <i class="fa-regular fa-copyright my-1 mx-2"></i>  2022 Football club - All Right Reserved.
    </div>

        
   
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

        .list-contatti{
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
            width: 450px;
            border-radius: 20px;
            padding: 1rem;
        }
       
        .list-footer li .item{
            list-style-type: square;
            margin: 1rem;
        }
        .list-footer li a{
            
            font-size: 15px;
            
           
        }
        .list-footer li a:hover{
            
           color: white;
           
        }

    
    }
</style>