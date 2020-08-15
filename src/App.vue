<style>
@import "./assets/style.css";
</style>
<template>
  <v-app>
    <v-main>
      <Header/>
    </v-main>
  </v-app>  
</template>

<script>
import Header from "@/components/Header";
import TypeEffect from './components/TypeEffect.vue'

export default {
  name: "App",
  components: {
    Header
  },

  data: () => ({
    //
  })
};
</script>
