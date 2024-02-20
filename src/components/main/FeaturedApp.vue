<script>

    export default {
        name: "FeaturedApp"
    }
</script>

<template>
    <div class="text-center mt-5">
        <div class="text-container p-2 mb-3">
            <h5 class="">Our Works</h5>
            <h2>Featured Productions</h2>
            <p>Here's just a small sample of some of those projects that we're quite proud of. If you're looking for something specific feel free to get in contact with us.</p>
        </div>
        <div class="row">
            <div class="col-3 offset-3">
                <div class="image-container position-relative">
                    <img src="../../assets/img/work1.png" alt="work 1">
                    <a href="#" class="position-absolute play-btn">
                        <i class="fa-solid fa-circle-play"></i>
                    </a>
                </div>
            </div>
            <div class="col-3">
                <div class="image-container-2 position-relative">
                    <img src="../../assets/img/work2.png" alt="work 2">
                    <a href="#" class="position-absolute play-btn-2">
                        <i class="fa-solid fa-circle-play"></i>
                    </a>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-3 offset-3">
                <div class="image-container position-relative">
                    <img src="../../assets/img/work3.png" alt="work 1">
                    <a href="#" class="position-absolute play-btn">
                        <i class="fa-solid fa-circle-play"></i>
                    </a>
                </div>
            </div>
            <div class="col-3">
                <div class="image-container-2 position-relative">
                    <img src="../../assets/img/work4.png" alt="work 2">
                    <a href="#" class="position-absolute play-btn-2">
                        <i class="fa-solid fa-circle-play"></i>
                    </a>
                </div>
            </div>
        </div>
        <button id="quote" class="mt-5">See Our work</button>
    </div>
</template>

<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;

.text-container{
    width: 30%;
    margin: 0 auto;
    h5{
        color:$purple;
    }
    h2{
    font-size: 100px;
    color: $aubergine;
    }
    p{
        color: $grey;
    }

}

.image-container {
    position: relative;
    overflow: hidden;
}

.play-btn{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%); 
        font-size: 2em;
        color: $purple;
        border-radius: 50px;
        // &:hover{

        // }
    }
    .play-btn-2{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%); 
        font-size: 2em;
        color: $purple;
        border-radius: 50px;
        // &:hover{

        // }
    }
    
    .image-container::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 99%;
    height: 100%;
    background-color: rgba(128, 0, 128, 0.3);
    opacity: 0;
    transition: opacity 0.5s ease;
    border-radius: 20px;
}

.image-container:hover::before {
    opacity: 1;
}


.image-container-2::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 99%;
    height: 100%;
    background-color: rgba(128, 0, 128, 0.3);
    opacity: 0;
    transition: opacity 0.5s ease;
    border-radius: 20px;
}

.image-container-2:hover::before {
    opacity: 1;
}


.play-btn, .play-btn-2 {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 2em;
    color: $purple;
    border-radius: 50px;
    z-index: 1;
}
#quote{
    z-index: 1;
    padding: 10px 30px;
    background-color: $white;
    border-radius: 50px;
    font-size: 20px;
    position: relative;
    transition: all 0.5s;
    color: #000000;
    border: 2px solid $grey;

    &:hover{
        color: white;
        background-color: $aubergine;
    }
}
</style>