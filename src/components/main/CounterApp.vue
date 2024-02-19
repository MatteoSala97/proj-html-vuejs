<script>

    export default {
        name: "CounterApp"
    }
</script>

<template>
    <div class="container-fluid text-center">
        <figure id="shape-top">
            <img src="../../assets/img/shape-top.png" alt="">
        </figure>
        <div class="container">
            <h2>ANIDIO Quick Facts</h2>
            <div class="row">
                <div class="col-3">
                    <div class="card border">
                        <h3>700+</h3>
                        <p>Projects Done</p>
                    </div>
                </div>
                <div class="col-3">
                    <div class="card border">
                        <h3>250+</h3>
                        <p>Happy Clients</p>
                    </div>
                </div>
                <div class="col-3">
                    <div class="card border">
                        <h3>25+</h3>
                        <p>Team Members</p>
                    </div>
                </div>
                <div class="col-3">
                    <div class="card border">
                        <h3>12+</h3>
                        <p>Years on the Market</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Globe Bg -->
        <figure id="globe">
            <img src="../../assets/img/globe.png" alt="">
        </figure>

        <!-- Shape Bottom -->
        <figure id="shape-bottom">
            <img src="../../assets/img/shape-bottom.png" alt="">
        </figure>
    </div>

</template>

<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;

.container-fluid{
    background-image: url(../../assets/img/preloader.png);
    height: 450px;
    margin-top: 75px;
    position: relative;

    #shape-top{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        
        img{
            width: 100%;
        }
    }

    #shape-bottom{
        position: absolute;
        bottom: -5%;
        left: 0;
        width: 100%;
        
        img{
            width: 100%;
        }
    }

    #globe{
        position: absolute;
        left: 40%;
        bottom: 15%;
        z-index: 0;
        
        img{
            width: 300px;
        }
    }
    
    h2{
        padding-top: 70px;
        margin-bottom: 40px;
    }

    h2,
    h3{
    font-size: 3em;
    font-weight: bolder;
    color: white;
}

    .card{
        background-color: rgba(0, 0, 0, 0);
        border-color: rgba(255, 255, 255, 0.5);
        padding-block: 40px;
        width: 90%;
        border-radius: 25px;
        transition: transform 0.3s ease;
        &:hover{
                transform: rotate(5deg);
        }

        p{
            color: $orange;
        }
    }
}

</style>