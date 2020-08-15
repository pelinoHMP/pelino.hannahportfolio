
<template>
  <!-- <v-app>
    <v-main>
      <Home/>
    </v-main>
  </v-app>-->
  <div>
      <Home></Home>
  </div>
</template>
<style scoped src="@/assets/style.css">
</style>
<script>
import Home from "./views/Home";
export default {
  name: "App",
  components: {
    Home
  },

  data: () => ({
    //
  })
};
</script>
