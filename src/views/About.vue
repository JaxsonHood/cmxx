<template>
  <div class="about mx-auto" style="background-color:#F5F5F5;">
    <div class="py-11"></div>

    <v-card
      class="mx-auto"
      outlined
      style="border-radius:18px; padding-top:60px; padding-bottom:65px; padding-left:8px; padding-right:8px;"
      :dark="true"
      max-width="1450"
    >
      <v-container class="text-center">
        <v-container class="text-center">
          <h2
            class="overline display-2 font-weight-bold mb-3"
            style="font-size:45px !important;"
          >Our Team</h2>
        </v-container>

        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-responsive
          class="mx-auto title font-weight-light mb-8"
          max-width="720"
        >We are a team of <span class='c_block' style="background-color:#FFE082; color:#263238;"> Computer Scientists </span> 
        seeking to help you achieve your digital platform goals. From full-scale applications, to simple blogs. We can create a <span class='c_block' style="background-color:#B3E5FC; color:black;"> Scalable </span>
        , <span class='c_block' style="background-color:#A5D6A7; color:black;"> Responsive </span>, 
        and <span class='c_block' style="background-color:#FFAB91; color:black;"> Innovative </span> solution to the challenges your business faces. Using up and coming web technologies we can meet the demands of an ever-changing online landscape.</v-responsive>

        <v-row mx-auto align="center" justify="center">
          <v-col v-for="(item,i) in theboys" :key="i" cols="12" sm="4" style="padding:5px; min-width:300px;" align="center" justify="center">
            <v-card
              class="mx-auto my-12"
              style="border-radius:20px; padding:5px;"
              max-width="330"
              :dark="true"
              outlined
              elevation="5"
            >
              <v-row mx-auto align="center" justify="center" style="height:210px; padding-top:15px;">
                <v-avatar color="orange" size="170">
                  <!-- <span class="white--text headline">170</span> -->
                  <v-img height="200" v-bind:src="require('../assets/' + item.img)"></v-img>
                </v-avatar>
              </v-row>

              <v-card-title
                class="justify-center overline"
                style="font-size:23px !important;"
              >{{item.name}}</v-card-title>
              <v-card-subtitle>
                <div class="text-center">{{item.role}}</div>
              </v-card-subtitle>
              <v-card-text>
                <div style="color:#EEEEEE;" class="text-center">{{item.writeup}}</div>
              </v-card-text>

              <v-divider class="mx-4"></v-divider>

              <v-card-title>
                <div style="color:#757575;">SPECIALTIES:</div>
              </v-card-title>

              <v-card-text>
                <v-chip-group column>
                  <v-chip
                    v-for="(skill,j) in item.skills"
                    :key="j"
                    :color="skill.color"
                    outlined
                  >{{skill.title}}</v-chip>
                </v-chip-group>
              </v-card-text>

              <v-card-actions>
                <!-- <v-btn
                    color="deep-purple lighten-2"
                    text
                    @click="reserve"
                  >
                    Reserve
                </v-btn>-->
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>

        <div></div>
        <!-- 
        <v-btn color="grey" href="https://vuetifyjs.com" outlined large>
          <span class="grey--text text--darken-1 font-weight-bold">Vuetify Documentation</span>
        </v-btn>-->
      </v-container>
    </v-card>

    <div class="py-8"></div>
  </div>
</template>

<style scoped>
 .c_block{
   font-weight:bold; border-radius:6px; margin-right:0.2em; margin-left:0.2em; display:inline-block; white-space: pre-wrap;
 }
</style>

<script>
// @ is an alias to /src
// import Card1 from "@/components/Card1.vue";

export default {
  name: "About",
  components: {
    // Card1
  },
  data() {
    return {
      theboys: [
        {
          name: "Jaxson Hood",
          role: "UX Designer / Software Developer",
          writeup:
            "As a team member at CMXX I believe in creating products that elevate the client experience, and an enviroment that pushes the team to new heights.",
          img: "jaxson.jpeg",
          skills: [
            {
              title: "UI Conception",
              color: "#EEEEEE"
            },
            {
              title: "Clean Design",
              color: "#EEEEEE"
            },
            {
              title: "Optimization",
              color: "#EEEEEE"
            },
            {
              title: "Proj. Organization",
              color: "#EEEEEE"
            }
          ]
        },
        {
          name: "Cameron Dickie",
          role: "UI Designer / Software Developer",
          writeup:
            "As a team member at CMXX I believe in creating products that elevate the client experience, and an enviroment that pushes the team to new heights.",
          img: "placeholder-profile.jpg",
          skills: [
            {
              title: "UI Conception",
              color: "#EEEEEE"
            },
            {
              title: "Clean Design",
              color: "#EEEEEE"
            },
            {
              title: "Optimization",
              color: "#EEEEEE"
            },
            {
              title: "Proj. Organization",
              color: "#EEEEEE"
            }
          ]
        },
        {
          name: "Alex Collins",
          role: "Business Lead / Product Consultant",
          writeup:
            "As a team member at CMXX I believe in creating products that elevate the client experience, and an enviroment that pushes the team to new heights.",
          img: "placeholder-profile.jpg",
          skills: [
            {
              title: "UI Conception",
              color: "#EEEEEE"
            },
            {
              title: "Clean Design",
              color: "#EEEEEE"
            },
            {
              title: "Optimization",
              color: "#EEEEEE"
            },
            {
              title: "Proj. Organization",
              color: "#EEEEEE"
            }
          ]
        }
      ]
    };
  }
};
</script>
