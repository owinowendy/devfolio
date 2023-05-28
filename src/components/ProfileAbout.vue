<template>
    <v-container fluid white>
        <v-layout row justify-center align-center class="mt-n12">
          <v-flex class="text-center mt-n12">
            <v-hover :close-delay="260" v-slot:default="{ hover }">
              <v-avatar
                :size="150"
                :class="[hover ? 'elevation-9' : 'elevation-5']"
              >
                <v-img :src="require('@/assets/wendy.jpeg')" alt="weny">
                  <template v-slot:placeholder>
                    <v-row class="fill-height ma-0" align="center" justify="center">
                      <v-progress-circular
                        indeterminate
                        color="light-blue accent-2"
                      ></v-progress-circular>
                    </v-row>
                  </template>
                </v-img>
              </v-avatar>
            </v-hover>
            <h4 class="title">{{ myName }}</h4>
            <p>{{ myJob }}</p>
          </v-flex>
    
          <v-flex xs11 md11 sm11 class="text-center">
            <div class="text-center">
              <h3 class="my-8z headline">About Me</h3>
              <!-- <h3 class="headline--text my-8 headline">About Me</h3> -->
            </div>
          </v-flex>
          <v-flex md9 xs9 sm9 justify-center align-center>
            <div class="text-center">
              <br />
              <p class="subheading text-left">{{ aboutMe }}</p>
              <p class="subheading text-left">{{ aboutMe2 }}</p>
              <p class="subheading text-left">{{ aboutMe3 }}</p>
              <p class="subheading text-left">{{ aboutMe4 }}</p>
            </div>
          </v-flex>
        </v-layout>
      </v-container>
    </template>
    <script>
    export default {
      data: function () {
        return {
          updateExists: false,
          myName: "Bhanji Wendy",
          myJob: "Front-End developer",
          aboutMe2:
            "I've worked with a wide variety of programming languages and frameworks such as HTML,CSS, JavaScript & PHP,Vuetify,Vuex. I believe that computing is affecting the lives of everyone on the planet and I think it is important to provide better tools/software program for people to access the potential offered by computer.",
          aboutMe3:
            "I am a goal-oriented engineer with a strong commitment in collaboration and solutions-oriented problem solving. I like building new stuff and work with other people – nothing really interesting is ever built alone! For me it is great to keep working on different skills, to meet new people and to contribute to make them happy.",
          aboutMe4:
            "I know that finding technical help is not the easiest thing, especially regarding something as specialized as language engineering. Hopefully I can be the right person to design and implement your projects. If not I will try my best to give you the right directions and help you find who can help you.",
          alignment: "center",
          dense: false,
          justify: "center",
        };
      },
      computed: {
        aboutMe() {
          return `Hi there, my name is Bhanji Wendy. I'm a Frontend Developer based in Nyeri, Kenya specializing in building and designing exceptional, high-quality websites and applications. I’ve been a  Frontend Developer from ${
            new Date().getFullYear() - 2021
          } years.`;
        },
      },
    };
    </script>
    