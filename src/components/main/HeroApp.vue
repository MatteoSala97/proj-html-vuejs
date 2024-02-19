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

        <div class="">
            <img src="https://pixner.net/anidio/carton-agency/assets/img/banner/middle.png" alt="Video logo">
            <a href="#"><i class="fas fa-circle-play"></i></a>
        </div>
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
</style>