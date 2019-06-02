<template>
  <v-app>
    <v-content>
      <CreationView/>
    </v-content>
  </v-app>
</template>

<script>
import CreationView from './components/CreationView'

export default {
  name: 'App',
  components: {
    CreationView,
  },
  data () {
    return {
      //
    }
  }
}
</script>
