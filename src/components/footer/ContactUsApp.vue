<script>
    export default {
        name: "ContactUsApp",
        data(){
            return{
                
            }
        }
    }
</script>

<template>
    <div class="d-flex justify-content-around align-items-center pt-4">
        <figure>
            <a href="#">
                <img src="../../assets/img/footer-logo.png" alt="Anidio Logo">
            </a>
        </figure>
        
        <ul class="d-flex gap-4 align-items-center">
            <li><a href="#">About Us</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Pricing</a></li>
            <li><a href="#">Career</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </div>
    <hr class="border w-50 m-auto my-4">
    <div class="container d-flex justify-content-between ">
        <span>Copyright © 2022 <span class="fw-bold" style="color:#4D36DC">Softivus</span>. All rights reserved. </span>

        <figure class="d-flex gap-5">
            <i class="fa-brands fa-facebook"></i>
            <i class="fa-brands fa-x-twitter"></i>
            <i class="fa-brands fa-instagram"></i>
        </figure>
    </div>
</template>

<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;

div{
    width: 80%;
    margin: 0 auto;
    top: 0;

    figure{
        z-index: 1;
    }
}

ul{
    li{
        z-index: 1;
            a{
            transition: color 0.3s ease;
            font-weight: bold;
            color: #000000;
                &:hover{
                color: $purple;
                cursor: pointer;
                }
            }
    }
}

.fa-brands{
    border: 1px solid $grey;
    background-color: $white;
    border-radius: 100px;
    color: $purple;
    padding: 5px;
    transition: background-color 0.3s ease-in;
    &:hover{
        background-color: $orange;
        color: $white;
        
    }
  }


</style>