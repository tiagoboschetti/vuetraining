<template>
  <v-app>
    <v-content>
      <CharCreation/>
    </v-content>
  </v-app>
</template>

<script>
import CharCreation from './components/CharCreation'

export default {
  name: 'App',
  components: {
    CharCreation
  },
  data () {
    return {
      //
    }
  }
}
</script>
