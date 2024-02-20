<script>

export default {
  name: "CarouselAppSecond",
  data() {
    return {
      
    };
  },
  created() {
    
  },
  methods: {
    
  }
};
</script>

<template>
    <div class="container mt-5 text-center" id="big-container">
        <img id="shape1" src="../../assets/img/shape.png" alt="shape">
        <img id="shape2" src="../../assets/img/shape2.png" alt="shape">
        <div>
            <h4>Anidio Magic Team Member</h4>
            <h2>Let Us Animate Your Project</h2>
            <p>We create new worlds! Let's collaborate and create engaging, effective, award-winning animations.</p>
        </div>
        <div class="d-flex justify-content-around pt-5" id="small-container">
            <div class="d-flex flex-column align-items-center ">
                <img src="../../assets/img/team1.png" alt="1">
                <h5 class="mt-3">Robert Coleman</h5>
                <span>
                    Owner & Creative Director
                </span>
                <figure class="d-flex gap-3">
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-x-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </figure>
            </div>
            <div class="d-flex flex-column align-items-center ">
                <img src="../../assets/img/team1.png" alt="1">
                <h5 class="mt-3">Hector Vargas</h5>
                <span>
                    Project Lead & Senior Animator
                </span>
                <figure class="d-flex gap-3">
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-x-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </figure>
            </div>
            <div class="d-flex flex-column align-items-center">
                <img src="../../assets/img/team2.png" alt="2">
                <h5 class="mt-3">Don Woods</h5>
                <span>
                    Administrator
                </span>
                <figure class="d-flex gap-3">
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-x-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </figure>
            </div>
            <div class="d-flex flex-column align-items-center">
                <img src="../../assets/img/team1.png" alt="3">
                <h5 class="mt-3">Thomas Nash</h5>
                <span>
                    2d Animator & Compositor
                </span>
                <figure class="d-flex gap-3">
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-x-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </figure>
            </div>
        </div>
        <div class="d-flex justify-content-center mt-4 align-items-center gap-2">
            <button>
                <i class="fa-solid fa-arrow-left border rounded-circle p-3"></i>
            </button>
            <div class="d-flex gap-3">
                <i class="fa-solid fa-circle"></i>
                <i class="fa-solid fa-circle"></i>
                <i class="fa-solid fa-circle"></i>
            </div>
            <button>
                <i class="fa-solid fa-arrow-right border rounded-circle p-3"></i>
            </button>
        </div>
    </div>
</template>
  
<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;
  
#big-container{
    position: relative;
}

#shape1{
    position: absolute;
    top: 0%;
    left: 0;
    z-index: -1;
}

#shape2{
    position: absolute;
    top: 0%;
    right: 0;
    z-index: -1;
}

button{
    background-color: $white;
    border-radius: 50px;
    color: $grey;
    &:hover{
        background-color: $orange;
        color: $white;
    }
  }

  .fa-brands{
    border: 1px solid $grey;
    background-color: $white;
    border-radius: 100px;
    color: $purple;
    padding: 5px;
    transition: background-color 0.3s ease-in;
    &:hover{
        background-color: $orange;
        color: $white;
        
    }
  }

  .fa-circle{
    font-size: 10px;
    color: $grey;
    &:hover{
        color: $orange;
        
    }
  }
</style>
  