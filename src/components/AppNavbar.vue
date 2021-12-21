<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-white">
    <div class="container-fluid">
      <router-link to="/">
        <figure class="mb-0">
          <img src="../assets/logo.png" alt="" />
        </figure>
      </router-link>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavDropdown"
        aria-controls="navbarNavDropdown"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav pe-0 mx-auto">
          <li class="navbar__link">
            <router-link to="/">الرئيسية</router-link>
          </li>
          <li class="navbar__link">
            <router-link to="/">التصنيفات</router-link>
          </li>
          <li class="navbar__link">
            <router-link to="/">التطبيقات</router-link>
          </li>
          <li class="navbar__link">
            <router-link to="/">طور تطبيق</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "AppNavbar",
};
</script>

<style scoped>
.navbar__link:not(:last-of-type) {
  padding-left: 100px;
}
.navbar__link a {
  color: black;
}
</style>
