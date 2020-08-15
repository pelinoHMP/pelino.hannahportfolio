<template>
  <v-footer dark padless>
    <center>
      <v-card class="black">
        <v-container>
          <v-row class="mb-12">
            <v-col v-for="item in icons" v-bind:key="item.icon">
              <v-btn :href="`${item.link}`" target="_blank">
                <v-icon size="24px">{{ item.icon }}</v-icon>
              </v-btn>
            </v-col>
          </v-row>
        </v-container>

        <v-card-text style="width:1345px;"
          class="white--text"
        >“Experience is the name everyone gives to their mistakes.”</v-card-text>
        <v-divider></v-divider>
        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} —
          <strong>This project is made with vue and vuetify</strong>
        </v-card-text>
      </v-card>
    </center>
  </v-footer>
</template>
<style scoped src="@/assets/style.css">
</style> 
<script>
export default {
  name: "Footer",
  data: () => ({
    icons: [
      {
        link: "https://www.facebook.com/hannahmae.pelino",
        icon: "mdi-facebook"
      },
      {
        link: "https://github.com/pelinohmp",
        icon: "mdi-github"
      },
      {
        link: "https://ph.linkedin.com/in/hannahmaepeliño",
        icon: "mdi-linkedin"
      },
      {
        link: "https://www.instagram.com/han_nah_meyy/",
        icon: "mdi-instagram"
      }
    ]
  })
};
</script>

