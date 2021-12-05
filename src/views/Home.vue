<template>
  <div>
    <navbar />
    <banner />
    <about />
    <us />
    <info />
  </div>
</template>

<script>
import Banner from "@/components/Banner.vue";
import Navbar from "@/components/Navbar.vue";
import About from "@/components/About.vue";
import Us from "../components/Us.vue";
import Info from "../components/Info.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    Banner,
    About,
    Us,
    Info,
  },
};
</script>
