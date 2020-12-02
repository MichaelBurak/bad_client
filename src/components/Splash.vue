<template>
    <v-content 
  :style="`background-image: url(${require('../assets/reagan-freeman-4Eu5Qsz7jmI-unsplash.jpg')})`" 
  class="fill-height bg-image" id="hello-content">
  <v-container justify-center fill-height>
    <v-row justify="center" align="center" style="background-color:white; opacity:.8;">
      <v-col cols="12" justify="center" style="border: 1px solid;">
        <p><h2> The most negative sounding U.S. headline this hour is: </h2> 
        
        <h1 style="font-weight: bold; color:purple;">
          <p>{{article}}</p>
            
        </h1>
<h2><span>(Photo by <a href="https://unsplash.com/@rfree18?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Reagan Freeman</a> on <a href="https://unsplash.com/s/photos/newspaper?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash)</a></span></h2>
      </v-col>
    </v-row>
  </v-container>
</v-content>
</template>

<script>
import axios from 'axios'
  export default {
    name: 'Splash',

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
   opacity: 0.8;
 }
 
</style>
