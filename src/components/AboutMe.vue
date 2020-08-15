<template>
  <div id="aboutMeSection">
    <v-container align="center" justify="center" id="aboutMe">
      <v-row justify="space-between">
        <v-col cols="auto">
          <v-img height="auto" max-width="400px" src="@/assets/wholebody.jpg"></v-img>
        </v-col>
        <v-col>
          <v-row class="flex-column ma-0 fill-height">
            <v-col class="px-9">
              <h1 class="h1">About Me</h1>
              <br>
              <div id="adjust">
                <p>An aspiring web developer seeking suitable environment which leads me to grow as a person. More sample text.More sample text.More sample text.More sample text.More sample text.</p>
                <p id="detailsAboutMe">
                  <span class="bold">Name:&nbsp;</span>Hannah Mae Pelino
                </p>
                <br>
                <p>
                  <span class="bold">Date of Birth:&nbsp;</span>July 24, 1999
                </p>
                <br>
                <p>
                  <span class="bold">Zip Code:&nbsp;</span>6000
                </p>
                <br>
                <p>
                  <span class="bold">Email Address:&nbsp;</span>email@gmail.com
                </p>
                <br>
                 <v-btn x-large color="primary" dark class="btnViewResume" href="https://www.canva.com/design/DAEE8mEwcEU/ZIbFWj1GCxbGaT7X-6bs-g/view?utm_content=DAEE8mEwcEU&utm_campaign=designshare&utm_medium=link&utm_source=sharebutton" target="_blank">View Resume</v-btn>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-row class="flex-column px-9 fill-height">
        <v-col class="px-9">
          <h1 class="header">Skills</h1>
          <br>
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
</template>
<style>
#aboutMeSection {
  margin-top: 660px;
}
.h1 {
  font-family: Arial, sans-serif;
  font-size: 60px;
  font-weight: 900;
  text-align: center;
}
#home {
  text-align: center;
  font-family: Arial, sans-serif;
  font-size: 20px;
  font-weight: 1000;
  color: blue;
}
#position {
  font-family: Arial, sans-serif;
  font-size: 2 0px;
  font-weight: 1000;
  color: #04458f;
}
h3 {
  font-family: Arial, sans-serif;
  font-size: 30px;
  font-weight: 1000;
  line-height: 1.5;
}
h4 {
  font-family: Arial, sans-serif;
  /* font-size: 30px; */
  font-weight: 1000;
  line-height: 1.5;
  color: #04458f;
}
.bold {
  font-weight: 600;
  color: #000;
  font-family: Arial, sans-serif;
}
.hannah {
  color: rgb(153, 153, 153);
  font-family: poppins, Arial, sans-serif;
  font-size: 16px;
  font-weight: 400;
  margin-top: 0px;
}
#detailsAboutMe {
  margin-top: 80px;
}
body {
  width: 100%;
  height: 100%;
}
.header {
  font-family: Arial, sans-serif;
  font-size: 50px;
  font-weight: 1000;
  line-height: 1.5;
}

.servicesIcon {
  display: flex;
  justify-content: center;
  width: 60px;
  height: auto;
}
.img {
  width: 200px;
  height: auto;
}
.cardService {
  padding: 40px;
  text-align: center;
}

#projectSection {
  max-width: 100%;
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
#canvas {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translateX(-50%) translateY(-50%);
  box-shadow: 0 0 10px 0 #999;
}
.btnSeeMore {
  position: absolute;
  top: 540px;
  left: 560px;
}
#adjust {
  font-size: 20px;
}
.btnViewResume{
  background-color: #04458f!important;
}
</style>

<script>
export default {
  name: "AboutMe",
  data: () => ({
    skills: [
      { src: "spython.png", flex: 2 },
      { src: "saspNet.png", flex: 2 },
      { src: "snodejs.png", flex: 2 },
      { src: "sjava.png", flex: 2 },
      { src: "stypescript.png", flex: 2 },
      { src: "sjs.png", flex: 2 },
      { src: "smongodb.png", flex: 2 },
      { src: "smssql.png", flex: 2 },
      { src: "svue.png", flex: 2 },
      { src: "sangular.png", flex: 2 },
      { src: "shtml.png", flex: 2 },
      { src: "srasp.png", flex: 2 },
      { src: "sPS.png", flex: 2 },
      { src: "sscratch.png", flex: 2 }
    ]
  })
};
</script>

<style scoped src="@/assets/style.css">
</style> 
