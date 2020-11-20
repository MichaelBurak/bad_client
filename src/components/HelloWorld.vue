<template>
<!--   
     <v-parallax
     height="100%"
    
    src="https://i.imgur.com/RtK5y6l.jpg"
  >

    <v-row
      align="center"
      justify="center"
    >
      <v-col
        class="text-center"
        cols="12"
      >
        <h1 class="display-1 font-weight-thin mb-4">
          {{article}}
        </h1>

      </v-col>
    </v-row>
  
     </v-parallax>
     -->
    <v-content 
  :style="`background-image: url(${require('../assets/reagan-freeman-4Eu5Qsz7jmI-unsplash.jpg')})`" 
  class="fill-height bg-image">
  <v-container justify-center fill-height>
    <v-row justify="center" align="center">
      <v-col cols="12" justify="center" style="border: 1px solid;">
        <p><h2> The most negative story right now is: </h2> 
        
        <h1 style="font-weight: bold; color:purple;">
          {{article}}
        </h1>

      </v-col>
    </v-row>
  </v-container>
</v-content>
</template>

<script>
import axios from 'axios'
  export default {
    name: 'HelloWorld',

    data: () => ({
      article:''
  }),
  created() {
  // Simple GET request using axios
  axios.get("https://bad-news-api.herokuapp.com/article")
    .then(response => this.article = response.data);
}
  }
</script>

<style>
 .bg-image {
   background-repeat: no-repeat;
   background-position: center center;
   background-attachment: fixed;
   background-size: cover;
   opacity: 0.5;
 }
</style>
