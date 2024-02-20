<script>

    export default {
        name: "HeroApp"
    }
</script>

<template>
    <div class="d-flex flex-column justify-content-center align-items-center gap-3">
        <h5>Imagine, Create, Experience</h5>
        <h1>We Animate</h1>
        <h1>With Ninja-Like Precision</h1>
        <p>
            We are a character-driven animation studio striving to make high-quality animations.
        </p>

        <div class="d-flex gap-4">
            <a class="btn" href="#"><span id="quote">Start a project</span></a>
            <a class="btn" href="#"><span id="quote-reverse">Portfolio</span></a>
        </div>

        <figure id="hero-thumb"  class="mt-5">
            <img src="https://pixner.net/anidio/carton-agency/assets/img/banner/middle.png" alt="Video logo">
            <a id="play-btn" href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">
                <i class="fa-solid fa-play"></i>
            </a>
        </figure>

        <!-- Background Items -->

        <!-- ASTRONAUTS -->
        <figure id="left-man">
            <img src="../../assets/img/left-man.png" alt="Astronaut on the left">
        </figure>
        <figure id="right-man">
            <img src="../../assets/img/right-man.png" alt="Astronaut on the right">
        </figure>

        <!-- GLOBES -->
        <figure id="globe-1">
            <img src="../../assets/img/globe1.png" alt="Planet number 1">
        </figure>
        <figure id="globe-2">
            <img src="../../assets/img/globe2.png" alt="Planet number 2">
        </figure>
        <figure id="globe-3">
            <img src="../../assets/img/globe3.png" alt="Planet number 3">
        </figure>

        <!-- DOTS -->
        <figure id="dots-left">
            <img src="../../assets/img/dots-left.png" alt="Stars and planets">
        </figure>
        <figure id="dots-right">
            <img src="../../assets/img/dots-right.png" alt="Stars and planets">
        </figure>

        <!-- UFO -->
        <figure id="ufo">
            <img src="../../assets/img/light.png" alt="Ufo">
        </figure>

        <!-- BOTTOM SHAPE -->
        <figure id="bottom-shape">
            <img src="../../assets/img/bottom-shape.png" alt="Wavy shaped background">
        </figure>
    </div>
</template>



<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;

div{
    padding-top: 50px;
    color: $white;

    h5{
        color: $orange;
    }
    h1{
        font-size: 100px;
        font-weight: bold;
    }
    p{
        font-size: 25px;
    }
}

.btn{
    z-index: 1;
    transition: color 0.3s ease;
    font-weight: bold;
    color: $white;
}

#quote{
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
        // border: 2px solid white;
    }
}

#quote-reverse{
    color: white;
    background-color: $aubergine;
    border: 2px solid white;
    padding: 10px 30px;
    font-size: 20px;
    border-radius: 50px;
    box-shadow: 0px 8px 18px 0px rgba(109, 100, 139, 0.61);
    border: 2px solid $pink;

    &:hover{
        transition: all 0.5s;
        color: #000000;
        background-color: $pink;
    }
}

    // Thumbnail Style
    figure{
        #hero-thumb{
            position: relative;
        }
    }

    // ASTRONAUTS

    // Left Man
    #left-man{
        position: absolute;
        top: 200px;
        left: 200px;
        animation: rotation 45s infinite linear;
        z-index: 2;

        img{
            width: 300px;
        }
    }

    // Right Man
    #right-man{
        position: absolute;
        top: 200px;
        right: 200px;
        animation: rotation 100s infinite linear;
       

        img{
            width: 300px
        }
    }

    // GLOBES

    // Globe 1
    #globe-1{
        position: absolute;
        top: 150px;
        left: 700px;
        animation: rotation 150s infinite linear;

        img{
            width: 180px
        }
    }

    // Globe 2
    #globe-2{
        position: absolute;
        top: 150px;
        right: 860px;
        animation: rotation 200s infinite linear;
        img{
            width: 140px
        }
    }

    // Globe 3
    #globe-3{
        position: absolute;
        top: -200px;
        right: 50%;
        animation: rotation 100s infinite linear;
        img{
            width: 300px
        }
    }

    // DOTS

    #dots-left,
    #dots-right{
        position: absolute;
        top: 0;
        width: 50%;
        z-index: 0;

        img{
            width: 100%;
        }
    }
    // Dots Left

    #dots-left{
        left: 0;
    }

    // Dots Right
    #dots-right{
        right: 0;
    }

    #ufo{
        position: absolute;
        top: 5%;
        right: 10%;
        animation: wiggle 2.5s infinite;
    }

    // Bottom Shape
    #bottom-shape{
        position: absolute;
        bottom: 27%;
        left: 0;
        width: 100%;
        z-index: 0;

        img{
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
    }


figure{
    z-index: 1;
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
            border-radius: 50px;
            padding: 10px 25px;
            background-color: #a616ea;
            animation: pulse 1s infinite;
        }
    }
    

</style>