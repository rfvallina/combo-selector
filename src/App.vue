<template>
<v-app>
  <v-content>
    <v-container>
      <v-layout row wrap>
        <v-flex xs8>
          <h1>Welcome to Vuetify!</h1>
        </v-flex>
      </v-layout>
    </v-container>
    <v-container>
      <v-layout row wrap>
        <v-flex xs8>
          <control></control>
        </v-flex>
      </v-layout>
    </v-container>
  </v-content>
  <v-footer app>
    <span>&copy; 2017</span>
  </v-footer>
</v-app>
</template>

<script>
import PrinterControl from './components/PrinterControl.vue';

export default {
  components: {
    'control': PrinterControl
  }
}
</script>
