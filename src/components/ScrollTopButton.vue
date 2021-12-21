<template>
  <button
    v-show="isScrolled"
    class="scroll__button justify-content-center align-items-center"
    @click="scrollToTop"
  >
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
  display: flex;
  left: 5px;
  bottom: 5px;
  width: 45px;
  height: 45px;
  border-radius: 50%;
  background-color: #ffd04c;
  border: none;
  font-size: 23px;
  color: #835d9d;
  z-index: 100;
}
</style>
