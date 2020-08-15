<template>
  <div>
    <Header></Header>
    <div id="first">
      <v-container>
        <img src="@/assets/first.png" id="firstappearance">
        <h1 class="headerName">Hi, I'm Hannah</h1>
        <h1 class="headerName2">Hi, I'm Hannah</h1>
        <!-- <p class="headerName3">I'm a Developer</p>
        -->

        <vue-typed-js
          :strings="['Web Developer.', 'Aspiring Photographer.', 'Doodle Artist.']"
          :backDelay="1000"
          :loop="true"
        >
          <h2 class="headerName3">
            A
            <span class="typing"></span>
          </h2>
        </vue-typed-js>
        <v-btn x-large color="primary" dark @click="gotoAboutMe()" class="btnSeeMore">See More</v-btn>
      </v-container>
    </div>

    <div>
      <AboutMe></AboutMe>
    </div>
    <!-- PROJECT SECTION -->
    <br>
    <div>
      <Project></Project>
    </div>
    <div>
      <Contact></Contact>
    </div>
    <div>
      <Footer></Footer>
    </div>
  </div>
</template>
 <style>
.h1 {
  font-family: Arial, sans-serif;
  font-size: 60px;
  font-weight: 900;
  text-align: center;
}

h3 {
  font-family: Arial, sans-serif;
  font-size: 30px;
  font-weight: 1000;
  line-height: 1.5;
}
body {
  width: 100%;
  height: 100%;
  font-family: Arial, sans-serif;
}
.header {
  font-family: Arial, sans-serif;
  font-size: 50px;
  font-weight: 1000;
  line-height: 1.5;
}
.img {
  width: 200px;
  height: auto;
}
#firstappearance {
  width: 1050px;
  height: auto;
  position: absolute;
  left: 10px;
  top: 50px;
}
.header {
  font-family: Arial, sans-serif;
  font-size: 50px;
  font-weight: 1000;
  line-height: 1.5;
  text-align: center;
}
.headerName {
  font-family: Arial, sans-serif;
  font-size: 70px;
  font-weight: 1000;
  line-height: 1.5;
  text-align: center;
  position: absolute;
  left: 630px;
  color: #cfe3ed;
  top: 200px;
}
.headerName2 {
  font-family: Arial, sans-serif;
  font-size: 70px;
  font-weight: 1000;
  line-height: 1.5;
  text-align: center;
  position: absolute;
  left: 634px;
  top: 200px;
  color: royalblue;
}
.headerName3 {
  font-family: Arial, sans-serif;
  font-size: 40px;
  font-weight: 900px;
  line-height: 1.5;
  text-align: center;
  position: absolute;
  left: 634px;
  top: 290px;
  color: black;
}
.btnSeeMore {
  position: absolute;
  top: 540px;
  left: 500px;
  width: 200px;
  background-color: rgb(96, 154, 230)!important;
}
</style> 

<script>
import VueTypedJs from "../components/VueTypedJs";
import AboutMe from "../components/AboutMe";
import Project from "../components/Project";
import Contact from "../components/Contact";
import Header from "../components/Header";
import Footer from "../components/Footer";

export default {
  components: {
    VueTypedJs,
    AboutMe,
    Project,
    Contact,
    Footer,
    Header
  },
  methods: {
    gotoAboutMe: function() {
      var element = document.getElementById("aboutMeSection");
      element.scrollIntoView();
      element.scrollIntoView({ behavior: "smooth" });
    }
  }
};
</script>