<template>
  <section class="UsContainer" id="us">
    <div class="container">
      <h2 class="UsContainer__titulo">Nuestro Equipo</h2>
      <div class="card-group">
        <card Nombre="Jahleel Solano" Perfil="Diseñador UX/UI, DIseador industrial y Desarrollador Frontend" Frase="Cada error te hace más fuerte"/>
        <card Nombre="David Pedraza" Perfil="Desarrollador Backend" Frase="frase"/>
        <card Nombre="Gabriela León" Perfil="Desarrolladora" Frase="frase"/>
        <card Nombre="Juan Gahona" Perfil="Desarrollador" Frase="frase"/>
        
      </div>
    </div>
  </section>
</template>

<script>
import Card from "./Card.vue";
export default {
  components: { Card },
  name: "Us",
  
};
</script>

<style>
.UsContainer {
  height: 85vh;
  background-color: #e3e3e3;
}
.UsContainer__titulo {
  color: #141414;
}
</style>
