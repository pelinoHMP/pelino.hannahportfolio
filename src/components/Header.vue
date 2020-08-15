<template>
  <div>
    <v-app-bar color="rgb(250, 255, 251)" inverted-scroll="true" fixed>
      <v-toolbar-title>H A N N A H</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-tab @click="gotoHome()">Home</v-tab>
      <v-tab @click="gotoAboutMe()">About</v-tab>
      <v-tab @click="gotoProject()">Projects</v-tab>
      <v-tab @click="gotoContact()">Contact</v-tab>
    </v-app-bar>
  </div>
</template>
<style scoped src="@/assets/style.css">
</style> 
<script>
export default {
  name: "Header",
  methods: {
    gotoAboutMe: function() {
      var element = document.getElementById("aboutMeSection");
      element.scrollIntoView();
      element.scrollIntoView({ behavior: "smooth" });
    },
    gotoHome: function() {
      var element = document.getElementById("first");
      element.scrollIntoView();
      element.scrollIntoView({ behavior: "smooth" });
    },
    gotoProject: function() {
      var element = document.getElementById("projectSection");
      element.scrollIntoView();
      element.scrollIntoView({ behavior: "smooth" });
    },
    gotoContact: function() {
      var element = document.getElementById("contactSection");
      element.scrollIntoView();
      element.scrollIntoView({ behavior: "smooth" });
    }
  }
};
</script>