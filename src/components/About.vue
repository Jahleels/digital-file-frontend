<template>
  <section class="aboutContainer">
    <div class="container">
      <h2 class="container__titulo">¿De qué trata?</h2>
    <b-button v-b-modal.modal-1>Launch demo modal</b-button>
    </div>

  <b-modal id="modal-1" title="BootstrapVue">
    <p class="my-4">Hello from modal!</p>
  </b-modal>
  </section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style>
.aboutContainer {
  height: 100vh;
  background-color: #9e2626;
}

.container {
  padding-top: 3rem;
}

.container__titulo {
  color: #f5f5f5;
  font-weight: 600;
  text-align: end;
  font-size: 3rem;
}
</style>
