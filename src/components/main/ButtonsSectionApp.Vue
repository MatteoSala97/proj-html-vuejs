<script>

    export default {
        name: "ButtonsSectionApp"
    }
</script>

<template>
<section class="big-container pb-5">
        <div class="container">
            <div class="section-header section-center">
                <h5 class="text-center text-primary">
                    Our Love For Animation
                </h5>
                <h2 class="text-center">
                    We're Storytelling Experts
                    With Creative Smarts
                </h2>
                <p class="text-center">
                    Our culture inspires the creative and innovative spirit found throughout our Studio.
                    We breathe life into new ideas!
                </p>
            </div>
            <div id="cards-container" class="row justify-content-around pt-5">
                <div class="col-lg-3 col-md-6 col-sm-9">
                    <div class="smart-items align-items-center text-center">
                        <figure class="thumb">
                            <img src="../../assets/img/smart1.png" alt="Magnifying glass logo">
                        </figure>
                        <div>
                            <h4>
                                <a href="#">3D modeling</a>
                            </h4>
                            <p>
                                We constantly ask questions. It helps us shape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.
                            </p>
                        </div>
                    </div>
                </div>
                <div class="col-lg-3 col-md-6 col-sm-9">
                    <div class="smart-items smart-items-two align-items-center text-center">
                        <figure class="thumb">
                            <img src="../../assets/img/smart2.png" alt="Collaboration logo">
                        </figure>
                        <div>
                            <h4>
                                <a href="#">Collaboration</a>
                            </h4>
                            <p>
                                We constantly ask questions. It helps us shape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.
                            </p>
                        </div>
                    </div>
                </div>
                <div class="col-lg-3 col-md-6 col-sm-9">
                    <div class="smart-items smart-items-three align-items-center text-center">
                        <figure class="thumb">
                            <img src="../../assets/img/smart3.png" alt="Creativity logo">
                        </figure>
                        <div>
                            <h4>
                                <a href="#">Creativity</a>
                            </h4>
                            <p>
                                We constantly ask questions. It helps us shape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="smart-man">
            <img src="../../assets/img/smart.png" alt="Kid with Vr-Headset">
        </div>
        <div class="rocket">
            <img src="../../assets/img/smart4.png" alt="rocket">
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;
.big-container{
    position: relative;
    padding-top: 400px;
    
}

h2{
    font-size: 90px;
    color: $aubergine;
}

#cards-container{
    width: 90%;
    margin: 0 20%;
}
.smart-items{
    display: flex;
    flex-direction: column;
    justify-content: center;
    border: 1px solid $grey;
    border-radius: 40px;
    padding: 35px 15px;
    background-color: $white;
    transition: all 0.3s;
    box-shadow: 0px 8px 18px 0px rgba(246, 243, 255, 0.61);
    background-image: -webkit-linear-gradient( 90deg, rgba(255,122,31,0.10196) 0%, rgba(1,5,48,0) 100%);
    
    &:hover{
        border: 1px solid $white;
        background-image: -webkit-linear-gradient( 90deg, rgba(1,5,48,0) 0%, rgba(255,122,31,0.10196) 100%);
    }
}
.smart-items-two{
    border: 1px solid $grey;
    background-image: -webkit-linear-gradient( 90deg, rgba(77,54,220,0.10196) 0%, rgba(1,5,48,0) 100%);
    box-shadow: 0px 8px 18px 0px rgba(246, 243, 255, 0.61);
    
    &:hover{
        background-image: -webkit-linear-gradient( 90deg, rgba(1,5,48,0) 0%, rgba(77,54,220,0.10196) 100%);
        border: 1px solid $white;
    }
}
.smart-items-three{
    border: 1px solid $grey;
    background-image: -webkit-linear-gradient( 90deg, rgba(255,0,15,0.10196) 0%, rgba(1,5,48,0) 100%);
    box-shadow: 0px 8px 18px 0px rgba(246, 243, 255, 0.61);
    
    &:hover{
        background-image: -webkit-linear-gradient( 90deg, rgba(1,5,48,0) 0%, rgba(255,0,15,0.10196) 100%); 
        border: 1px solid $white;
    }
}

.smart-man{
    position: absolute;
    left: 0;
    top: 20%;
    img{
        width: 700px;
    }
}
.rocket{
    position: absolute;
    right: 0;
    bottom: 0;
    img{
        width: 100px;
    }
}

</style>