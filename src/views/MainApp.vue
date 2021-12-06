<template>
  <div class="MainApp container">
    <h1>
      DigitalFile
      <span> @Beta 1.1 </span>
    </h1>

    <b-button v-b-modal.modal-1
      ><b-icon icon="folder-plus"></b-icon> Agregar nuevo archivo</b-button
    >

    <!-- Modal -->
    <b-modal id="modal-1" title="Subir archivo">


      <form @submit.prevent="guardar" enctype="multipart/form-data">
        <!-- Input archivo -->
        <div class="input-group mb-3">
          <input type="file" ref="file" @change="selectFile" class="form-control" />
        </div>

        </form>

        <label class="form-label mb-2"
          >Escoge un nombre de la categoría y un color (opcional)</label
        >
        <div class="d-flex justify-content mb-3">
          <!-- Input color -->
          <input
            type="color"
            class="form-control form-control-color"
            value="#e3e3e3"
            title="Escoge tu color"
          />
          <!-- Input categoria -->
          <input
            type="text"
            class="form-control ms-2"
            placeholder="Categoría"
          />
        </div>

      <!-- Botones del modal -->
      <template v-slot:modal-footer="{ guardar, cancel }">
        <b-button @click="guardar" variant="primary">Enviar</b-button>
        <b-button @click="cancel()" variant="light">Cancelar</b-button>
      </template>
      
    </b-modal>





    <!-- Mostrar archivos -->
    <b-card-group columns>
    <card-archivos />
    </b-card-group>

  </div>
</template>

<script>
import CardArchivos from '../components/CardArchivos.vue';
export default {
  components: { CardArchivos },
  name: "HelloWorld",

  data() {
    return {
      file: "",
      // file:File
    };
  },
  methods: {
    selectFile() {
      console.log(this.file);
      this.file = this.$refs.file.files[0];
    },
    // async sendFile() {
    //   console.log("Send");
    //   const formData = new FormData();
    //   formData.append("file", this.file);
    //   try {
    //     const response = await axios.get("http://localhost:5000/test");
    //     const response = await axios.post(
    //       "http://localhost:5000/upload",
    //       formData
    //     );
    //     console.log(response);
    //   } catch (error) {
    //     console.log(error.message);
    //   }
    // },

    guardar: function (e) {
      console.log("Send");
      let obj = new FormData();
      obj.append("archivo", this.file);
      this.archivoMongo
        .post("http://localhost:5000/book", obj)
        .then((respone) => {
          console.log(respone.data);
        });
      e.preventDefault();
    },

    getArchivo: function () {
      this.archivoMongo.get("http://localhost:5000/book").then((respone) => {
        console.log(respone);
        let url = "abc";
        console.log(url);
      });
    },
  },
};
</script>

<style scoped>
html {
  background-color: #e3e3e3;
}
h1 {
  font-family: "BoutiqueScript";
  font-size: 5rem;
}
span {
  font-family: "Courier New", Courier, monospace;
  font-size: 12pt;
}
</style>