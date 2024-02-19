<script>

    export default {
        name: "HeroApp"
    }
</script>

<template>
    <div class="d-flex flex-column justify-content-center align-items-center">
        <h5>Imagine, Create, Experience</h5>
        <h1>We Animate</h1>
        <h1>With Ninja-Like Precision</h1>
        <p>
            We are a character-driven animation studio striving to make high-quality animations.
        </p>

        <div class="d-flex gap-4">
            <button>Start a project</button>
            <button>Portfolio</button>
        </div>

        <figure id="hero-thumb"  class="">
            <img src="https://pixner.net/anidio/carton-agency/assets/img/banner/middle.png" alt="Video logo">
            <a id="play-btn" href="#">
                <i class="fa-solid fa-play"></i>
            </a>
        </figure>
    </div>
    



</template>



<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;

div{
    color: $white;
    h5{
        color: $orange;
    }
}

figure{
        position: relative;
        
        img{
            display: block;
        }

        #play-btn{
            position: absolute;
            top: 45%;
            left: 47%;
            transform: translate(-50%, -50%); 
            font-size: 2em;
            color: $white;
            border-radius: 500px;
            padding: 10px 20px;
            background-color: #a616ea;
            animation: pulse 1.5s infinite;
        }
    }

    @keyframes pulse {
        0% {
            transform: scale(.9) ;
            box-shadow: 0 0 0 rgba(166, 22, 234, 0.7);
        }
        50% {
            transform: scale(1.1) ;
            box-shadow: 0 0 0 50px rgba(#a616ea, 0);
        }
        100% {
            transform: scale(1) ;
            box-shadow: 0 0 0 50px rgba(#a616ea, 0);
        }
    }

</style>