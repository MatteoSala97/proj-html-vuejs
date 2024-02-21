<script>

export default {
  name: "CarouselAppSecond",
  data() {
    return {
        currentIndex: 0,
        timer: null,
      slides:[
        {
            image: "src/assets/img/team1.png",
            name: "Robert Coleman",
            role: "Owner & Creative Director",

        },
        {
            image: "src/assets/img/team2.png",
            name: "Hector Vargas",
            role: "Project Lead & Senior Animator",

        },
        {
            image: "src/assets/img/team1.png",
            name: "Don Woods",
            role: "Administrator",

        },
        {
            image: "src/assets/img/team2.png",
            name: "Thomas Nash",
            role: "2d Animator & Compositor",

        },
      ]
    };
  },
  mounted: function() {
    this.startSlide()
  },
  methods: {
    startSlide: function(){
      this.timer = setInterval(this.next, 3000)
    },
    next: function(){
      if(this.currentIndex === this.slides.length - 1){
        this.currentIndex = 0
      } else{
        this.currentIndex ++
      }
    },
    prev: function(){
      if((this.currentIndex - 1) < 0){
        this.currentIndex = this.slides.length - 1
      } else{
        this.currentIndex --
      }
    }
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
            <div class="d-flex flex-column align-items-center">
                <img :src="slides[currentIndex].image" alt="1">
                <h5 class="mt-3">{{ slides[currentIndex].name }}</h5>
                <span>
                    {{ slides[currentIndex].role }}
                </span>
                <figure class="d-flex gap-3 mt-2">
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-x-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </figure>
            </div>
            <div class="d-flex flex-column align-items-center ">
                <img :src="slides[(currentIndex + 1) % slides.length].image" alt="1">
                <h5 class="mt-3">{{ slides[(currentIndex + 1) % slides.length].name }}</h5>
                <span>
                    {{ slides[(currentIndex + 1) % slides.length].role }}
                </span>
                <figure class="d-flex gap-3 mt-2">
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-x-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </figure>
            </div>
            <div class="d-flex flex-column align-items-center">
                <img :src="slides[(currentIndex + 2) % slides.length].image" alt="3">
                <h5 class="mt-3">{{ slides[(currentIndex + 2) % slides.length].name }}</h5>
                <span>
                    {{ slides[(currentIndex + 2) % slides.length].role }}
                </span>
                <figure class="d-flex gap-3 mt-2">
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-x-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </figure>
            </div>
        </div>
        <div class="d-flex justify-content-center mt-4 align-items-center gap-2">
            <button>
                <i class="fa-solid fa-arrow-left border rounded-circle p-3" @click="prev"></i>
            </button>
            <div class="d-flex gap-3">
                <i class="fa-solid fa-circle"></i>
                <i class="fa-solid fa-circle"></i>
                <i class="fa-solid fa-circle"></i>
            </div>
            <button>
                <i class="fa-solid fa-arrow-right border rounded-circle p-3" @click="next"></i>
            </button>
        </div>
    </div>
</template>
  
<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;
  
#big-container{
  padding-top: 80px;
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

    h4{
      color: $purple;
    }
    h2{
        font-size: 100px;
        font-weight: bold;
        color: $aubergine;
    }
    h3{
        font-size: 30px;
        font-weight: bold;
    }
    p{
        font-size: 25px;
    }
</style>
  