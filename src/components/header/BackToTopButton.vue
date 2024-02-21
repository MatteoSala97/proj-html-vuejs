<script>
export default {
  name: "BackToTopButton",
  data() {
    return {
      showButton: false
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.scrollY > 300) {
        this.showButton = true;
      } else {
        this.showButton = false;
      }
    },
    backToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    }
  }
};
</script>

<template>
  <div>
    <button v-if="showButton" @click="backToTop" id="back-to-top-btn">
      <i class="fa-solid fa-arrow-up"></i>
    </button>
  </div>
</template>


<style lang="scss" scoped>
@use "../../assets/styles/general.scss" as *;
@use "../../assets/styles/partials/mixins.scss" as *;
  
  #back-to-top-btn {
  position: fixed;
  bottom: 20px;
  right: 25px;
  background-color: $purple;
  padding: 10px 17px;
  border-radius: 50px;
  color: $white;
  &:hover{
    color: $orange;
    background-color: $white;
    border: 1px solid $grey;
    box-shadow: rgba(0,0,0,0.3);
  }
}
</style>
