<template>
  <app-navbar />
  <router-view />
  <scroll-top-button />
  <chat-button />
  <app-footer />
</template>

<script>
import AppNavbar from "./components/AppNavbar.vue";
import AppFooter from "./components/AppFooter.vue";
import ScrollTopButton from "./components/ScrollTopButton.vue";
import ChatButton from "./components/ChatButton.vue";

export default {
  name: "App",
  components: {
    AppNavbar,
    AppFooter,
    ScrollTopButton,
    ChatButton,
  },
};
</script>

<style></style>
