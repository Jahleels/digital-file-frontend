<template>
  <nav
    class="navbar navbar-expand-lg navbar-dark"
    style="background-color: #141414"
  >
    <div class="container-fluid">
      <router-link to="/" class="navbar-brand">
        <img src="" />
      </router-link>
      <router-link class="navbar-brand mb-0 " to="/"
        >Digital File</router-link
      >
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <router-link class="nav-link" to="/">De que trata</router-link>
          <router-link class="nav-link" to="/">Quienes somos</router-link>
          <router-link class="nav-link" to="/">Más información</router-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
.navbar-brand {
    font-family: 'BoutiqueScript';
    font-size: 3rem !important;
    margin-right: 2rem !important;
}


</style>
