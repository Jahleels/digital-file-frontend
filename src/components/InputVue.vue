<template>
  <section class="container">
    <div class="input-group">
      <input
        type="file"
        class="form-control mb-3"
        id="inputGroupFile04"
        aria-describedby="inputGroupFileAddon04"
        aria-label="Upload"
      />
    </div>


    <label for="exampleColorInput" class="form-label mb-2">Escoge un nombre de la categoría y un color</label>
    <div class="d-flex justify-content mb-3">
        
    <input
      type="color"
      class="form-control form-control-color"
      id="exampleColorInput"
      value="#563d7c"
      title="Escoge tu color"
    />
    <input
      type="text"
      class="form-control ms-2"
      placeholder="Categoría"
      aria-label="Dependencia"
    />
    </div>
  </section>
</template>

<script>
export default {
  name: "InputVue",
};
</script>

<style>
</style>