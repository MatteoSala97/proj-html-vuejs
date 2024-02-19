<script>

    export default {
        name: "HeaderApp"
    }
</script>

<template>
    <div class="d-flex justify-content-around align-items-center pt-2">
        <figure>
            <img src="../../assets/img/logo.png" alt="Anidio Logo">
        </figure>
        
        <ul class="d-flex gap-3">
            <li><a href="#">Home</a></li>
            <li><a href="#">About Us</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Our Process</a></li>
            <li><a href="#">Pricing</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Contact</a></li>
            <li>
                <button>Get a Quote</button>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;

</style>