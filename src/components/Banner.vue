<template>
  <header class="bg-primary">
    <div class="container">
      <div>
        <div class="contenedorPrincipal">
          <h1>¡Haz un espacio a tu medida!</h1>
          <p>
            Digital File fue creado para personas quienes quieren (y ahora pueden) organizar sus archivos de forma sencilla, !y muy fácil! La tecnología ofrece formas muy intuitivas de resolver los problemas y este software te ayudará a tener tu espacio limpio y ordenado a tu gusto.
          </p>
          <!--Botón-->
        </div>

        <div></div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Banner",
};
</script>

<style scoped>
header {
  background-image: url("../assets/background-banner.jpg");
  background-position: center;
  height: 87vh;
  padding-top: 20vh;
}
.contenedorPrincipal {
  background-color: rgba(227, 227, 227, 0.8);
  padding: 16px;
  width: 35rem;
  border-radius: 4px;
}
</style>
