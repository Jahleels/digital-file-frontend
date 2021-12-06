<template>
      <b-card
      style="max-width:10rem;"
        :border-variant="colorArchivo"
        :header="categoria"
        :header-bg-variant="colorArchivo"
        header-text-variant="white"
        align="center"
      >
        <b-card-text>{{nombreArchivo}}</b-card-text>
      </b-card>
</template>

<script>
export default {
    name: "CardArchivos",
    data: () =>{ return {
        nombreArchivo: 'Mi archivo.pdf',
        colorArchivo: 'primary',
        categoria: 'Categoría'
        }
    }
}
</script>

