<template>
    <v-container fluid light-blue accent-1>
      <v-layout row justify-center align-center>
        <v-flex xs11 md11 sm11 class="text-center">
          <div class="text-center">
            <h3 class="my-8 headline">Work Experience</h3>
          </div>
        </v-flex>
        <v-flex md8 xs11 mb-11 class="text-center">
          <v-timeline>
            <v-timeline-item
              v-for="(work, i) in works"
              :key="i"
              :icon="work.icon"
              :color="work.color"
              fill-dot
            >
              <template v-slot:opposite>
                <span
                  :class="`headline font-weight-bold `"
                  v-text="work.year"
                ></span>
              </template>
              <div class="py-4">
                <h2
                  :class="`headline font-weight-light mb-4`"
                  v-text="work.work"
                ></h2>
                <div>
                  <h4 class="subtitle-1">{{ work.where }}</h4>
                  <p class="caption">{{ work.addr }}</p>
                </div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-flex>
      </v-layout>
    </v-container>
  </template>
  <script>
  export default {
    data: () => ({
      works: [
        {
          color: "blue",
          icon: "mdi-briefcase-account",
          year: "17/01/2022 - 31/08/2022",
          work: "Technical Writer",
          where: "Sectio.io.engineering",
          addr: "",
        },
        {
          color: "green",
          icon: "mdi-briefcase-account",
          year: "01/09/2021 - 01/09/2022",
          work: "FrontEnd Developer",
          where: "Bikebuka Company",
          addr: "",
        },
      ],
    }),
  };
  </script>
  