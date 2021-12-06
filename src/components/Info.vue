<template>
  <section class="InfoContainer">
    <div class="container">
      <h1 class="InfoContainer__titulo">¡Contactanos y sé parte!</h1>
      <div class="mb-3">
        <label for="" class="form-label" style="color: #f5f5f5"
          >Dirección de correo electrónico</label
        >
        <input
          type="email"
          class="form-control"
          id=""
          placeholder="nombre@ejemplo.com"
        />
      </div>
      <div class="mb-3">
        <label for="" class="form-label" style="color: #f5f5f5"
          >Escribenos!</label
        >
        <textarea class="form-control" id="" rows="3"></textarea>
      </div>
      <b-button variant="primary">Enviar</b-button>
    </div>
  </section>
</template>

<script>
export default {
  name: "Info",
};
</script>

<style>
.InfoContainer {
  height: 60vh;
  background-color: #141414;
}
.InfoContainer__titulo {
  color: #f5f5f5;
  text-align: center;
}
</style>