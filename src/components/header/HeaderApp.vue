<script>

    export default {
        name: "HeaderApp"
    }
</script>

<template>
    <div class="d-flex justify-content-around align-items-center pt-4">
        <figure>
            <a href="#">
                <img src="../../assets/img/logo.png" alt="Anidio Logo">
            </a>
        </figure>
        
        <ul class="d-flex gap-4 align-items-center">
            <li><a href="#">Home</a></li>
            <li><a href="#">About Us</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Our Process</a></li>
            <li><a href="#">Pricing</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Contact</a></li>
            <li>
                <a class="btn"><span id="quote">Get a Quote</span></a>
            </li>
        </ul>
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
            color: $white;

                &:hover{
                color: $orange;
                }
            }
    }
}

#quote{
    z-index: 1;
    padding: 10px 30px;
    background-color: $pink;
    border-radius: 50px;
    font-size: 20px;
    position: relative;
    transition: all 0.5s;
    color: #000000;
    box-shadow: 0px 8px 18px 0px rgba(109, 100, 139, 0.61);
    border: 2px solid $pink;

    &:hover{
        color: white;
        background-color: $aubergine;
    }
}
</style>