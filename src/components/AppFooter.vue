<template>
  <footer class="main__footer d-flex flex-column align-items-center">
    <figure class="footer__logo">
      <img src="../assets/footer/footer-logo.png" alt="" />
    </figure>
    <ul
      class="footer__socialLinks list-unstyled d-flex justify-content-center p-0 mb-0"
    >
      <li>
        <router-link to="/"><fa :icon="['fab', 'twitter']" /></router-link>
      </li>
      <li>
        <router-link to="/"><fa :icon="['fab', 'instagram']" /></router-link>
      </li>
      <li>
        <router-link to="/"><fa :icon="['fab', 'linkedin-in']" /></router-link>
      </li>
      <li>
        <router-link to="/"><fa :icon="['fab', 'youtube']" /></router-link>
      </li>
    </ul>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style scoped>
.main__footer {
  padding-top: 30px;
  padding-bottom: 90px;
  background-color: #835d9d;
}
.footer__logo {
  margin-bottom: 35px;
}
.footer__socialLinks > li:not(:first-child) {
  padding-right: 45px;
}
.footer__socialLinks > li > a {
  color: white;
}
.footer__socialLinks > li > a svg {
  transition: all 0.3s ease-in-out;
}
.footer__socialLinks > li > a:hover svg {
  transform: translateY(-5px);
}
</style>
