<template>
  <div class="MainApp container">
    <h1>DigitalFile
      <span>
       @Beta 1.1
      </span>
    </h1>

    <b-button v-b-modal.modal-1
      ><b-icon icon="folder-plus"></b-icon> Agregar nuevo archivo</b-button
    >

    <b-modal id="modal-1" title="Subir archivo">
      <form @submit.prevent="sendFile" enctype="multipart/form-data">
        <div class="input-group">
          <input
            class="form-control mb-3"
            type="file"
            ref="file"
            @change="selectFile"
          />
        </div>
        <label for="exampleColorInput" class="form-label mb-2"
          >Escoge un nombre de la categoría y un color (opcional)</label
        >
        <div class="d-flex justify-content mb-3">
          <input
            type="color"
            class="form-control form-control-color"
            value="#e3e3e3"
            title="Escoge tu color"
          />
          <input
            type="text"
            class="form-control ms-2"
            placeholder="Categoría"
          />
        </div>
        <div class="d-flex justify-content-end"></div>
      </form>
      <template v-slot:modal-footer="{ sendFile, cancel }">
        <b-button @click="sendFile()" variant="primary">Enviar</b-button>
        <b-button @click="cancel()" variant="light">Cancelar</b-button>
      </template>
    </b-modal>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "HelloWorld",

  data() {
    return {
      file: "",
    };
  },
  methods: {
    selectFile() {
      console.log(this.file);
      this.file = this.$refs.file.files[0];
    },
    async sendFile() {
      console.log("Send");
      const formData = new FormData();
      formData.append("file", this.file);
      try {
        // const response = await axios.get("http://localhost:5000/test");
        const response = await axios.post(
          "http://localhost:5000/upload",
          formData
        );
        console.log(response);
      } catch (error) {
        console.log(error.message);
      }
    },
  },
};
</script>

<style scoped>
html {
  background-color: #e3e3e3;
}
h1 {
  font-family: 'BoutiqueScript';
  font-size: 5rem;
}
span {
  font-family:'Courier New', Courier, monospace;
  font-size: 12pt;
}
</style>