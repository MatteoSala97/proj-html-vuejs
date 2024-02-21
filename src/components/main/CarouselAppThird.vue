<script>

export default {
  name: "CarouselAppThird",
  data() {
    return {
      currentIndex: 0,
      timer: null,
      slides:[
        "src/assets/img/sponsor1.png",
        "src/assets/img/sponsor2.png",
        "src/assets/img/sponsor3.png",
        "src/assets/img/sponsor4.png",
        "src/assets/img/sponsor5.png",
        "src/assets/img/sponsor6.png"
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
        <div class="w-50 m-auto">
            <h4>Why Anidio studio?</h4>
            <h2>We Love Our Clients</h2>
            <p>We are trusted throughout adland and have a wealth of recommendations from star-ups to renowned global brands.</p>
        </div>
        <div class="d-flex justify-content-around pt-5" id="small-container">
            <div class="d-flex flex-column align-items-center ">
                <img :src="slides[currentIndex]" alt="1">
            </div>
            <div>
                <img :src="slides[(currentIndex + 1) % slides.length]" alt="2">
            </div>
            <div>
                <img :src="slides[(currentIndex + 2) % slides.length]" alt="3">
            </div>
            <div>
                <img :src="slides[(currentIndex + 3) % slides.length]" alt="4">
            </div>
            <div>
                <img :src="slides[(currentIndex + 4) % slides.length]" alt="5">
            </div>
            <div>
                <img :src="slides[(currentIndex + 5) % slides.length]" alt="6">
            </div>
        </div>
    </div>
</template>
  
<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;
  

</style>
  