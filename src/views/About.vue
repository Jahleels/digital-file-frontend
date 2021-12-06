<template>
  <div class="about">
    <h1>This is an about page</h1>
      <form @submit.prevent="guardar" enctype="multipart/form-data">
        <input type="file" ref="file" @change="selectFile" />
        <button @submit.prevent="guardar" type="submit">Enviar</button>
      </form>
  </div>
</template>

<script>
// import axios from "axios";
export default {
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

    guardar:function(e){
      console.log("Send");
      let obj = new FormData()
      obj.append("archivo",this.file)
      this.archivoMongo.post("http://localhost:5000/book", obj).then (respone => {
        console.log(respone.data);
      })
      e.preventDefault();
    },

    getArchivo:function(){
      this.archivoMongo.get("http://localhost:5000/book").then(respone => {
        console.log(respone)
        let url = "abc";
        console.log(url);
      })
    }
  },
};
</script>

<style scoped>
</style>
