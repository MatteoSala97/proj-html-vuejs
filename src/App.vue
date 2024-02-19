<script>
import HeaderApp from './components/header/HeaderApp.vue';
import HeroApp from './components/main/HeroApp.vue';

  export default{
    components:{
      HeaderApp,
      HeroApp
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
</template>

<style lang="scss">
@use "./assets/styles/general.scss";

header{
  background: url(./assets/img/banner-bg.png);
  background-size: cover;
  background-repeat: no-repeat;
  height: 600px;
}

</style>


vbase