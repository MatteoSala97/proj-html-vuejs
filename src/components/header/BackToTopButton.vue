<script>
  export default {
    name: "BackToTopButton",
    data() {
      return {
        showButton: false
      };
    },
    methods: {
     
    },
    mounted() {
     
    },
  };
  </script>

<template>
    <button @click="scrollToTop" v-show="showButton" id="back-to-top-btn">
      Back to Top
    </button>
</template>
  
<style lang="scss">
  #back-to-top-btn {
    position: fixed;
    bottom: 20px;
    right: 20px;
    display: none;
    color: black;
}
</style>
  