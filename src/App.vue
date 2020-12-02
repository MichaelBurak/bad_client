<template>
  <v-app>
    <v-main>
      <Splash/>
    </v-main>
  </v-app>
</template>

<script>
import Splash from './components/Splash'

export default {
  name: 'App',

  components: {
    Splash,
  },

  data: () => ({
    //
  }),
};
</script>
