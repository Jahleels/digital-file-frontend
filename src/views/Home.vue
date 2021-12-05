<template>
  <div>
    <navbar />
    <banner />
  </div>
</template>

<script>
import Banner from "@/components/Banner.vue";
import Navbar from "@/components/Navbar.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    Banner,
  },
};
</script>
