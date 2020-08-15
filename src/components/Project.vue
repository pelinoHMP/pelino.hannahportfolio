<template>
  <div id="projectSection">
    <br>
    <h1 class="header">My Projects</h1>
    <br>
    <center>
      <p
        class="text-center"
      >As an aspiring web/software developer, doing projects makes me sharpen my skills.</p>
    </center><br>
    <v-container>
      <v-row dense>
        <v-col v-for="(card, i ) in cards" :key="i" :cols="card.flex">
          <v-hover v-slot:default="{ hover }" open-delay="100">
            <v-card :elevation="hover ? 20 : 4" style="box-shadow: 10px 10px 5px #aaaaaa;">
              <v-img
                :src="require(`@/assets/${card.src}`)"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="200px"
              ></v-img>
              <v-card-title v-text="card.title"></v-card-title>
              <v-card-subtitle v-text="card.description"></v-card-subtitle>
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>
    <br>
  </div>
</template>

<style scoped src="@/assets/style.css">
</style> 
<script>
export default {
  name: "Project",
  data: () => ({
    cards: [
      {
        title: "BHManagement",
        src: "bhm.jpeg",
        flex: 4,
        description:
          "Enable the landlords to monnitor ther own borders using the system."
      },
      {
        title: "Rentahi",
        src: "rentahi.jpg",
        flex: 4,
        description:
          "Enable user to post, shop and rent the things they wanted to using this system."
      },
      {
        title: "Chat",
        src: "chat.jpeg",
        flex: 4,
        description:
          "The project number Three is three.The project number Three is three the project."
      }
    ]
  })
};
</script>

