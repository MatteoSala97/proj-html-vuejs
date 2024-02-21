<script>
export default {
  name: "CarouselAppFirst",
  data() {
    return {
      currentIndex: 0,
      timer: null,
      slides:[
        {
          image: "src/assets/img/process1.png",
          phrase: "We'll take your idea and create a technical script which consists of action notes and animation description",
          badge: "1"
        },
        {
          image: "src/assets/img/process2.png",
          phrase: "We'll take your idea and create a technical script which consists of action notes and animation description",
          badge: "2"
        },
        {
          image: "src/assets/img/process1.png",
          phrase: "We'll take your idea and create a technical script which consists of action notes and animation description",
          badge: "3"
        },
        {
          image: "src/assets/img/process2.png",
          phrase: "We'll take your idea and create a technical script which consists of action notes and animation description",
          badge: "4"
        },
      ]
    };
  },
  mounted: function() {
    this.startSlide()
  },
  methods: {
    startSlide: function(){
      this.timer = setInterval(this.next, 1000)
    },
    next: function(){
      if(this.currentIndex + 1 == this.slides.length){
        this.currentIndex = 0 
      } else{
        this.currentIndex = this.currentIndex + 1
      }
    },
    prev: function(){
      if((this.currentIndex - 1) < 0){
        this.currentIndex = this.slides.length - 1
      } else{
        this.currentIndex = this.currentIndex - 1
      }
    }
  }
};
</script>

<template>
    <div id="big-container " class="row mt-5 mb-5">
      <div class="col-6">
        <figure id="rocket">
          <img src="../../assets/img/process-thumb.png" alt="Girl riding a rocket">
        </figure>
      </div>
        <div class="small-container col-4">
            <div class="text-container text-center">
                <h5>Our Process</h5>
                <h2>Our Process for Your Animation Production</h2>
                <p>We have an effective process for working on animation</p>
            </div>
            <div class="row">
                <div class="col-5 d-flex flex-column align-items-center text-center border rounded-4 p-4" id="card"
                v-for="i in [currentIndex]" :key="i"
                >
                    <img :src="slides[i +1 ].image" alt="1">
                    <h2 class="mt-2">Scripting</h2>
                    <p>We'll take your idea and create a technical script which consists of action notes and animation description</p>
                    <span id="badge">1</span>
                  </div>
                  <div class="col-5 offset-1 d-flex flex-column align-items-center text-center border rounded-4 p-4" id="card"
                  v-for="i in [currentIndex]" :key="i">
                    <img :src="slides[i].image" alt="2">
                    <h2 class="mt-2">Pre-Production</h2>
                    <p>We'll take your idea and create a technical script which consists of action notes and animation description</p>
                    <span id="badge">2</span>
                  </div>
                <div class="d-flex gap-3 justify-content-start mt-4">
                    <button>
                        <i class="fa-solid fa-arrow-left border rounded-circle p-3" @click="prev"></i>
                    </button>
                    <button>
                        <i class="fa-solid fa-arrow-right border rounded-circle p-3" @click="next"></i>
                    </button>
                </div>
            </div>
        </div> 
    </div>
  </template>
  
  <style lang="scss" scoped>
  @use "../../assets/styles/general.scss" as *;
  @use "../../assets/styles/partials/mixins.scss" as *;
  
  #big-container {
    width: 80%;
    margin: 0 auto; 
}
#rocket{
    margin-left: 300px;
}

.small-container{
    margin-top: 150px;
}

#card{
    position: relative;
}
#card img{
    height: 100px;
}

  #badge{
    border-radius: 50px;
    position: absolute;
    top: 5%;
    right: 5%;
    background-color: $almostWhite;
    border-radius: 150px;
    padding: 10px 15px;
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
  </style>
  