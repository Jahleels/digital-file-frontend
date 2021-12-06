<template>
  <header class="bg-primary">
    <div class="container">
      <div>
        <div class="contenedorPrincipal">
          <h1>Haz un espacio a tu medida!</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Necessitatibus molestiae obcaecati sit. Inventore dolores expedita
            sit tempora velit distinctio corrupti. Cupiditate commodi tempora
            ipsa vitae laudantium suscipit repudiandae mollitia fuga. Inventore
            ab sequi ipsum perferendis nemo quaerat recusandae amet delectus
            totam minima culpa quibusdam laudantium, commodi illo vel. Vitae
            molestiae autem consequuntur illum. Molestiae, distinctio maxime.
            Rem quod culpa incidunt?
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
