<template>
  <div class="card">
    <img src="../assets/logo.jpg" class="card-img-top" />
    <div class="card-body">
      <h5 class="card-title">{{Nombre}}</h5>
      <p class="card-text">
        {{Perfil}}
      </p>
      <p class="card-text">
        <small class="text-muted">{{Frase}}</small>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props:[
      'Nombre',
      'Perfil',
      'Frase'
  ]
  
};
</script>

<style>
.card {
  margin: 1rem 2rem 0 2rem;
}
</style>
