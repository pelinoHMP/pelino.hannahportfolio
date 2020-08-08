<template>
  <div>
    <v-app-bar color="#e1e0de">
      <v-toolbar-title>H A N N A H</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-tab @click="goto('/home')">Home</v-tab>
      <v-tab>About</v-tab>
      <v-tab>Resume</v-tab>
      <v-tab>Projects</v-tab>
      <v-tab>Contact</v-tab>
    </v-app-bar>
  </div>
</template>
<style scoped src="@/assets/style.css">
</style>
<script>
export default {
  name: "Header",
  methods: {
    goto(link) {
      this.$route.path == link ? "" : this.$router.push(link);
    }
  }
};
</script>
