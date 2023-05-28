<template>
    <v-container fluid light-blue lighten-5>
      <v-layout row justify-center justify-space-around mb-5>
        <v-flex xs12 md11 sm11 class="text-center">
          <div class="text-center">
            <h3 class="mt-8 headline">Technical Skills</h3>
          </div>
        </v-flex>
        <!-- programming language and frameworks -->
        <v-flex md3 xs9 sm9>
          <h4 class="title my-8 text-center gray--text">
            Programming and Frameworks
            <span>
              <p class="body-1">Program & frameworks I frequently use.</p>
            </span>
          </h4>
          <div class="text-center">
            <v-chip-group column>
              <v-tooltip bottom v-for="prg in programing" :key="prg.lang">
                <template v-slot:activator="{ on }">
                  <v-chip
                    color="white"
                    pill
                    icon
                    v-on="on"
                    @click="redirect(prg.link)"
                  >
                    <v-avatar color="teal lighten-4" left>
                      <v-img :src="require(`@/assets/icons/${prg.icon}`)"></v-img>
                    </v-avatar>
                    {{ prg.lang }}
                  </v-chip>
                </template>
                <span>Click to view more info</span>
              </v-tooltip>
            </v-chip-group>
          </div>
        </v-flex>
        <!-- TOOLS -->
        <v-flex md3 xs9 sm9>
          <h4 class="title my-8 text-center gray--text">
            Tools and Libraries
            <span>
              <p class="body-1">Tools and libraries I frequently use.</p>
            </span>
          </h4>
          <div class="text-center">
            <v-chip-group column>
              <v-tooltip bottom v-for="tool in tools" :key="tool.lang">
                <template v-slot:activator="{ on }">
                  <v-chip
                    color="white"
                    pill
                    icon
                    v-on="on"
                    @click="redirect(tool.link)"
                  >
                    <v-avatar color="teal lighten-4" left>
                      <v-img
                        :src="require(`../assets/icons${tool.icon}`)"
                      ></v-img>
                    </v-avatar>
                    {{ tool.lang }}
                  </v-chip>
                </template>
                <span>Click to view more info</span>
              </v-tooltip>
            </v-chip-group>
          </div>
        </v-flex>
  
        <v-flex md3 xs9 sm9>
          <h4 class="title my-8 text-center gray--text">
            Other Stuff
            <span>
              <p class="body-1">I do extra things like:</p>
            </span>
          </h4>
          <v-chip-group column>
            <v-chip
              color="white"
              pill
              icon
              v-for="stuff in otherStuffs"
              :key="stuff"
            >
              <v-avatar color="blue" left>
                <v-icon color="white">mdi-star</v-icon>
              </v-avatar>
              {{ stuff }}
            </v-chip>
          </v-chip-group>
        </v-flex>
      </v-layout>
    </v-container>
  </template>
  <script>
  export default {
    data() {
      return {
        programing: [
         
          {
            icon: "react-icon.png",
            lang: "React JS",
            link: "https://reactjs.org/",
          },
          {
            icon: "Vue.js_Logo_2.svg",
            lang: "Vue JS",
            link: "https://vuejs.org/",
          },
          {
            icon: "angular.png",
            lang: "Angular2+",
            link: "https://angular.io/",
          },
          {
            icon: "laravel.png",
            lang: "Laravel",
            link: "https://laravel.com/",
          },
          {
            icon: "nodejs-icon.svg",
            lang: "Node Js",
            link: "https://nodejs.org/",
          },
          {
            icon: "vuetify.svg",
            lang: "Vuetify",
            link: "https://vuetifyjs.com/en/",
          },
          {
            icon: "nuxt-js.png",
            lang: "Nuxt JS",
            link: "https://nuxtjs.org/",
          },
          {
            icon: "sql.svg",
            lang: "SQL",
            link: "https://en.wikipedia.org/wiki/Microsoft_SQL_Server",
          },
          {
            icon: "HTML5_logo_and_wordmark.svg",
            lang: "HTML5",
            link: "https://en.wikipedia.org/wiki/HTML5",
          },
          {
            icon: "javascript-736400_960_720.webp",
            lang: "JavaScript",
            link: "https://en.wikipedia.org/wiki/JavaScript",
          },
          {
            icon: "php-logo.svg",
            lang: "PHP",
            link: "https://www.php.net/docs.php",
          },
         
          {
            icon: "jQuery.gif",
            lang: "JQuery",
            link: "https://jquery.com/",
          },
        ],
        tools: [
          {
            icon: "sqlServer.png",
            lang: "Microsoft SQL Server 2016 - Developer",
            link: "https://www.microsoft.com/en-us/sql-server/sql-server-2016",
          },
          {
            icon: "xampp-logo.svg",
            lang: "XAMPP",
            link: "https://www.apachefriends.org/index.html",
          },
         
          {
            icon: "webpack.png",
            lang: "Webpack",
            link: "https://webpack.js.org/",
          },
          {
            icon: "IIS.png",
            lang: "Internet Information Services (IIS)",
            link: "https://visualstudio.microsoft.com/vs/",
          },
          {
            icon: "vs2019.svg",
            lang: "Visual Studio 2019",
            link: "https://visualstudio.microsoft.com/vs/",
          },
          {
            icon: "VsCode.png",
            lang: "Visual Studio Code",
            link: "https://visualstudio.microsoft.com/vs/",
          },
        ],
        otherStuffs: [
          "Format Computer",
          "Configure Computer Network",
          "Computer Hardware troubleshoot",
        ],
      };
    },
    methods: {
      redirect(link) {
        if (!link || link.length <= 0) return;
        window.open(link, "_blank");
      },
    },
  };
  </script>
 