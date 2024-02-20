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
                <figure>
                    <img src="../../assets/img/work1.png" alt="work 1">
                </figure>
            </div>
            <div class="col-6">
                <figure>
                    <img src="../../assets/img/work2.png" alt="work 2">
                </figure>
            </div>
        </div>
        <div class="row">
            <div class="col-3 offset-3">
                <figure>
                    <img src="../../assets/img/work3.png" alt="work 3">
                </figure>
            </div>
            <div class="col-6">
                <figure>
                    <img src="../../assets/img/work4.png" alt="work 4">
                </figure>
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