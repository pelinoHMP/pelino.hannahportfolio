<template>
  <div>
    <v-app-bar color="#d9d8d7" inverted-scroll="true" fixed>
      <v-toolbar-title>H A N N A H</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-tab @click="goto('/home')">Home</v-tab>
      <v-tab @click="gotoAboutMe">About</v-tab>
      <v-tab @click="gotoProject">Projects</v-tab>
      <v-tab @click="gotoContact">Contact</v-tab>
    </v-app-bar>
    <div id="home">
      <h2>Hey! I'm Hannah</h2>
      <h4 id="position">I'm a</h4>
      <span class="typed-text">{{ typeValue }}</span>
      <span class="cursor" :class="{'typing': typeStatus}">&nbsp;</span>
    </div>
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
                <p>An aspiring web developer seeking suitable environment which leads me to grow as a person. More sample text.More sample text.More sample text.More sample text.More sample text.</p>
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
        <v-row class="flex-column px-9 fill-height">
          <v-col class="px-9">
            <h3>Skills</h3>
            <br>
            <!-- <v-img class="img" src="@/assets/education.png"></v-img> -->
            <v-row class="mx-12 sm-9">
              <v-col v-for="(skill, i ) in skills" :key="i" :cols="skill.flex">
                <v-img class="skillIcon" :src="require(`@/assets/${skill.src}`)"></v-img>
              </v-col>
            </v-row>
            <br>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <br>
    <br>
    <!-- PROJECT SECTION -->
    <br>
    <div id="projectSection">
      <br>
      <h1 class="header">Our Projects</h1>
      <p
        class="text-center"
      >Far far away, behind the word mountains, far from the countries Vokalia and Consonantia</p>
      <v-container fluid class="designShadow">
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
    <div id="contactSection">
      <br>
      <h1 class="header">Contact Me</h1>
      <p
        class="text-center"
      >Far far away, behind the word mountains, far from the countries Vokalia and Consonantia</p>
      <v-container fluid class="contact">
        <v-row>
          <v-col cols="auto">
            <v-img height="auto" max-width="400px" src="@/assets/wholebody.jpg"></v-img>
          </v-col>
          <v-col>
            <v-text-field label="Your Name" outlined></v-text-field>
            <v-text-field label="Your Email" outlined></v-text-field>
            <v-text-field label="Subject" outlined></v-text-field>
            <v-textarea
              v-model="bio"
              auto-grow
              outlined
              color="deep-purple"
              label="Message"
              rows="7"
            ></v-textarea>
            <v-btn large color="#04458F" dark class="my-2">SEND MESSAGE</v-btn>
          </v-col>
        </v-row>
      </v-container>
      <br>
    </div>
    <v-footer dark padless>
      <v-card flat tile class="black white--text text-center">
        <v-card-text>
          <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>
        <v-card-text
          class="white--text pt-0"
        >Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.</v-card-text>
        <v-divider></v-divider>
        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} —
          <strong>Vuetify</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </div>
</template> <style scoped src="@/assets/style.css">
</style> 
<script>
import { setTimeout } from 'timers';
  export default {
    data: () => {
      return {
        typeValue: '',
        typeStatus: false,
        typeArray: ['fun', 'awesome', 'a journey', 'life'],
        typingSpeed: 200,
        erasingSpeed: 100,
        newTextDelay: 2000,
        typeArrayIndex: 0,
        charIndex: 0
      }
    },
    methods: {
      typeText() {
        if(this.charIndex < this.typeArray[this.typeArrayIndex].length) {
          if(!this.typeStatus)
            this.typeStatus = true;
          this.typeValue += this.typeArray[this.typeArrayIndex].charAt(this.charIndex);
          this.charIndex += 1;
          setTimeout(this.typeText, this.typingSpeed);
        }
        else {
          this.typeStatus = false;
          setTimeout(this.eraseText, this.newTextDelay);
        }
      },
      eraseText() {
        if(this.charIndex > 0) {
          if(!this.typeStatus)
            this.typeStatus = true;
          this.typeValue = this.typeArray[this.typeArrayIndex].substring(0, this.charIndex - 1);
          this.charIndex -= 1;
          setTimeout(this.eraseText, this.erasingSpeed);
        }
        else {
          this.typeStatus = false;
          this.typeArrayIndex += 1;
          if(this.typeArrayIndex >= this.typeArray.length)
            this.typeArrayIndex = 0;
          setTimeout(this.typeText, this.typingSpeed + 1000);
        }
      }
    },
    created() {
      setTimeout(this.typeText, this.newTextDelay + 200);
    }
  }
export default {
  data: () => ({
    skill: 20,
    knowledge: 33,
    power: 78,
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
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
    ],
    skills: [
      { src: "spython.png", flex: 2 },
      { src: "sjava.png", flex: 2 },
      { src: "snodejs.png", flex: 2 },
      { src: "sscratch.png", flex: 2 },
      { src: "stypescript.png", flex: 2 },
      { src: "shtml.png", flex: 2 },
      { src: "srasp.png", flex: 2 }
    ]
  }),
  methods: {
    gotoAboutMe: function() {
      var element = document.getElementById("aboutMeSection");
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