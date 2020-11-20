<template>
  <div>
    {{article}}
    </div>
    
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
