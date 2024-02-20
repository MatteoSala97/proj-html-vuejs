<script>

    export default {
        name: "FormApp"
    }
</script>

<template>
    <div class="container-fluid text-center">
        <figure id="shape-top">
            <img src="../../assets/img/shape-top.png" alt="wavy top background">
        </figure>
        <div class="container pt-5">
            <h5>We Create New Worlds</h5>
            <h2>Want Tips On Your Storytelling?</h2>
            <p>Join our newsletter for tips on how to elevate your brand through storytelling</p>
            <form action="#" class="flex-form">
                <input type="email" placeholder="Enter your email">
                <button type="submit">
                    <span>
                        Submit
                    </span>
                </button>
            </form>
        </div>
        <!-- Shape Bottom -->
        <figure id="shape-bottom">
            <img src="../../assets/img/shape-bottom.png" alt="Wavy bottom background">
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
    background-repeat: no-repeat;
    background-size: cover;

    #shape-top{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        
        img{
            width: 100%;
        }
    }
    h5{
        color: $orange;
        font-size: 35px;
    }
    h2,p{
        color: $white;
    }
    h2{
        font-size: 90px;
        width: 60%;
        margin: 0 auto;
    }
    .flex-form{
        position: relative;
    }

    input{
        width: 600px;
        border-radius: 50px;

        padding: 10px 15px;
    }
    button{
        position: absolute;
        top: 10%;
        right: 28%;
        border-radius: 20px;
        padding: 5px 20px;
        background-color: $pink;
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

    
}

</style>