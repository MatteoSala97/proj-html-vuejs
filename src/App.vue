<script>
import HeaderApp from './components/header/HeaderApp.vue';
import HeroApp from './components/main/HeroApp.vue';
import ButtonsSectionApp from './components/main/ButtonsSectionApp.vue';
import CounterApp from './components/main/CounterApp.vue';
import FeaturedApp from './components/main/FeaturedApp.vue';
import CarouselAppFirst from './components/main/CarouselAppFirst.vue';
import CarouselAppSecond from './components/main/CarouselAppSecond.vue';
import CarouselAppThird from './components/main/CarouselAppThird.vue';

  export default{
    components:{
      HeaderApp,
      HeroApp,
      ButtonsSectionApp,
      CounterApp,
      FeaturedApp,
      CarouselAppFirst,
      CarouselAppSecond,
      CarouselAppThird,
    },
    data(){
      return{
        
      }
    },
    methods:{
      
    }
  }
</script>

<template>
  <header>
    <HeaderApp/>
    <HeroApp/>
  </header>
  <main>
    <ButtonsSectionApp/>
    <CounterApp/>
    <FeaturedApp/>
    <CarouselAppFirst/>
    <CarouselAppSecond/>
    <CarouselAppThird/>
  </main>
</template>

<style lang="scss">
@use "./assets/styles/general.scss";

header{
  background: url(./assets/img/banner-bg.png);
  background-size: cover;
  background-repeat: no-repeat;
  height: 900px;
}

</style>


vbase