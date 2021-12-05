<template>
    <section class="UsContainer">
        <div class="container">
            <h2 class="UsContainer__titulo" >
                Nuestro Equipo
            </h2>
            <div class="card-group">
                <card />
                <card />
                <card />
                <card />
            </div>

        </div>
    </section>
</template>

<script>
import Card from './Card.vue';
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