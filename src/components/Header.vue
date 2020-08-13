<template>
  <div>
    <v-app-bar color="#BFC5C9" fixed>
      <v-toolbar-title>H A N N A H</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-tab @click="goto('/home')">Home</v-tab>
      <v-tab @click="gotoAboutMe">About</v-tab>
      <v-tab @click="gotoService">Services</v-tab>
      <v-tab @click="gotoProject">Projects</v-tab>
      <v-tab>Contact</v-tab>
    </v-app-bar>

    <div id="aboutMeSection">
      <v-container align="center" justify="center" id="aboutMe">
        <v-row justify="space-between">
          <v-col cols="auto">
            <v-img height="auto" max-width="400px" src="@/assets/wholebody.jpg"></v-img>
          </v-col>
          <v-col>
            <v-row class="flex-column ma-0 fill-height">
              <v-col class="px-9">
                <h1>About Me</h1>
                <p>
                  An aspiring web developer seeking suitable environment which leads me to grow as a person.
                  More sample text.More sample text.More sample text.More sample text.More sample text.
                </p>
                <p id="detailsAboutMe">
                  <span class="bold">Name:&nbsp;</span>Hannah Mae Pelino
                </p>
                <p>
                  <span class="bold">Date of Birth:&nbsp;</span>July 24, 1999
                </p>
                <p>
                  <span class="bold">Zip Code:&nbsp;</span>6000
                </p>
                <p>
                  <span class="bold">Email Address:&nbsp;</span>email@gmail.com
                </p>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
        <v-row class="flex-column px-9 fill-height">
          <v-col class="px-9">
            <h3>Education</h3>
            <br>
            <!-- <v-img class="img" src="@/assets/education.png"></v-img> -->
            <v-row class="mx-12">
              <v-card class="col-12 mx-12">
                <h4>2019- Present</h4>
                <v-card-title class="headline">Certificate of Computer Technology(CCT)</v-card-title>
                <v-card-subtitle>University of San Carlos- Talamban Campus</v-card-subtitle>
              </v-card>
            </v-row>
            <br>
          </v-col>
        </v-row>
        <v-row class="flex-column px-9 fill-height">
          <v-col class="px-9">
            <h3>Experience</h3>
            <br>
            <!-- <v-img class="img" src="@/assets/education.png"></v-img> -->
            <v-row class="mx-12">
              <v-card class="col-12 mx-12">
                <h4>2019- Present</h4>
                <v-card-title class="headline">Intern at Lear Corporation</v-card-title>
                <v-card-subtitle>PETC, Lear 1, Lapu-lapu City</v-card-subtitle>
              </v-card>
            </v-row>
            <br>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <br>
    <br>
    <!-- SERVICE SECTION -->

    <div>
      <h1 class="header" id="serviceSection">Services</h1>
      <p
        class="text-center"
      >Far far away, behind the word mountains, far from the countries Vokalia and Consonantia</p>
      <v-container fluid class>
        <v-row>
          <v-col v-for="(service, i ) in services" :key="i" :cols="service.flex">
            <v-hover v-slot:default="{ hover }" open-delay="100">
              <v-card :elevation="hover ? 20 : 2" class="mx-auto cardService">
                <center>
                  <v-img class="servicesIcon" justi :src="require(`@/assets/${service.src}`)"></v-img>
                </center>
                <v-card-title v-text="service.title" class="justify-center"></v-card-title>
                <v-card-subtitle v-text="service.description"></v-card-subtitle>
              </v-card>
            </v-hover>
          </v-col>
        </v-row>
      </v-container>
    </div>

    <!-- PROJECT SECTION -->
    <br>
    <div id="projectSection">
      <br>
      <h1 class="header">Our Projects</h1>
      <p
        class="text-center"
      >Far far away, behind the word mountains, far from the countries Vokalia and Consonantia</p>
      <v-container fluid>
        <v-row dense>
          <v-col v-for="(card, i ) in cards" :key="i" :cols="card.flex">
            <v-hover v-slot:default="{ hover }" open-delay="100">
              <v-card :elevation="hover ? 20 : 2">
                <v-img
                  :src="card.src"
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
    <p>vfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvnvfiovfkdvfkvnfjvn</p>
  </div>
</template>
<style scoped src="@/assets/style.css">
</style>
<script>
export default {
  data: () => ({
    skill: 20,
    knowledge: 33,
    power: 78,
    cards: [
      {
        title: "BHManagement",
        src:
          "https://images.pexels.com/photos/1797393/pexels-photo-1797393.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
        flex: 4,
        description:
          "Enable the landlords to monnitor ther own borders using the system."
      },
      {
        title: "Rentahi",
        src:
          "https://images.pexels.com/photos/4506249/pexels-photo-4506249.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
        flex: 4,
        description:
          "Enable user to post, shop and rent the things they wanted to using this system."
      },
      {
        title: "Project Three",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 4,
        description:
          "The project number Three is three.The project number Three is three the project."
      }
    ],
    services: [
      {
        title: "Web Design",
        flex: 4,
        src: "analysis.png",
        description:
          "Enable the landlords to monnitor ther own borders using the system."
      },
      {
        title: "App Developing",
        flex: 4,
        src: "idea.png",
        description:
          "Enable user to post, shop and rent the things they wanted to using this system."
      },
      {
        title: "Web Developing",
        flex: 4,
        src: "code.png",
        description:
          "The project number Three is three.The project number Three is three the project."
      },
      {
        title: "Web Design",
        flex: 4,
        src: "analysis.png",
        description:
          "Enable the landlords to monnitor ther own borders using the system."
      },
      {
        title: "App Developing",
        flex: 4,
        src: "idea.png",
        description:
          "Enable user to post, shop and rent the things they wanted to using this system."
      },
      {
        title: "Web Developing",
        flex: 4,
        src: "code.png",
        description:
          "The project number Three is three.The project number Three is three the project."
      }
    ]
  }),
  methods: {
    gotoAboutMe: function() {
      var element = document.getElementById("aboutMeSection");
      element.scrollIntoView();
      element.scrollIntoView({
        behavior: "smooth"
      });
    },
    gotoService: function() {
      var element = document.getElementById("serviceSection");
      element.scrollIntoView();
      element.scrollIntoView({
        behavior: "smooth"
      });
    },
    gotoProject: function() {
      var element = document.getElementById("projectSection");
      element.scrollIntoView();
      element.scrollIntoView({
        behavior: "smooth"
      });
    }
  }
};
</script>
