<template>
  <center>
    <div id="contactSection">
      <br>
      <h1 class="header">Contact Me</h1>
      <center>
        <p class="text-center">With the use of the internet, connect me with no worries.</p>
      </center>
      <v-container fluid class="contact" justify-center="center">
        <v-row>
          <v-col cols="auto">
            <v-img height="auto" max-width="400px" src="@/assets/wholebody.jpg"></v-img>
          </v-col>
          <v-col>
            <v-text-field label="Your Name" outlined></v-text-field>
            <v-text-field label="Your Email" outlined></v-text-field>
            <v-text-field label="Subject" outlined></v-text-field>
            <v-textarea auto-grow outlined color="deep-purple" label="Message" rows="7"></v-textarea>
            <v-btn large color="#04458F" dark class="my-2">SEND MESSAGE</v-btn>
          </v-col>
        </v-row>
      </v-container>
      <br>
    </div>
  </center>
</template>
<style>
#contactSection {
  max-width: 900px;
}
</style> 
<script>
export default {
  name: "Contact",
  data: () => ({})
};
</script>
