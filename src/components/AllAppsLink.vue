<template>
  <div class="page__appLinkWrapper">
    <router-link class="page__appLink" to="/">
      <span>تصفح التطبيقات</span>
      <span
        ><fa class="chevron__animation" :icon="['fas', 'chevron-left']"
      /></span>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "AllAppsLink",
};
</script>

<style lang="scss" scoped>
.page__appLink {
  background-color: $mainColor;
  padding: 13px 65px;
  border-radius: 10px;
  span {
    color: $subColor;
    font-size: 18px;
    font-weight: 700;
    &:last-child {
      font-size: 16px;
      font-weight: 400;
      padding-right: 12px;
    }
    .chevron__animation {
      animation-name: chevron__animation;
      animation-duration: 0.4s;
      animation-iteration-count: infinite;
    }
    @keyframes chevron__animation {
      0% {
        transform: scale(1);
      }
      100% {
        transform: scale(1.25);
      }
    }
  }
}
</style>
