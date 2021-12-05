<template>
  <nav
    class="navbar navbar-expand-lg navbar-dark"
    style="background-color: #141414"
  >
    <div class="container-fluid">
      <router-link class="navbar-brand mb-0" to="/">Digital File</router-link>

      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <a class="nav-link" href="#">De que trata</a>
          <a class="nav-link" href="#">Quienes somos</a>
          <a class="nav-link" href="#">Más información</a>
        </div>
        <button class="btn btn-outline-danger ms-4">¡Probarlo Ya!</button>
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
  font-family: "BoutiqueScript";
  font-size: 3rem !important;
  margin-right: 2rem !important;
  margin-left: 2rem !important;
}
</style>
