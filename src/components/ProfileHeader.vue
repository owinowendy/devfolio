<template>
    <v-container class="mt-5">
      <v-parallax
      dark
    height="700"
    src="../assets/bakground.jpg"
      >
    <v-layout align-center class="text-center darken-3" justify-center>
      <v-flex md6 xs11 sm11>
        <h1 class="display-1 font-weight-thin mb-4" v-text="message"></h1>
        <h4 class="headline" v-text="description"></h4>
      </v-flex>
    </v-layout>
  </v-parallax>
    </v-container>
</template>
<script>
export default{
data(){
return {
    message:"Hi ,I'm Wendy",
    description:"Front-End developer majoring in Vue js,Vuetify,javascript,Html& Cssframeworks  "
}
}
}
</script> 