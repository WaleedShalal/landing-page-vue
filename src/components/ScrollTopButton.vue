<template>
  <button v-show="isScrolled" class="scroll__button" @click="scrollToTop">
    <fa :icon="['fas', 'arrow-up']" />
  </button>
</template>

<script>
export default {
  name: "ScrollTopButton",
  data() {
    return {
      isScrolled: true,
    };
  },
  methods: {
    scrollToTop: function () {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
    getPageYOffset: function () {
      window.onscroll = () => {
        let distanceFromTop = window.pageYOffset;
        this.isScrolled = distanceFromTop > 0 ? true : false;
        return this.isScrolled;
      };
    },
  },
  mounted() {
    this.getPageYOffset();
  },
};
</script>

<style lang="scss" scoped>
.scroll__button {
  position: fixed;
  left: 5px;
  bottom: 5px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: #ffd04c;
  border: none;
  font-size: 25px;
  color: #835d9d;
  z-index: 100;
}
</style>
