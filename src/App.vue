<template>
  <v-app>
    <v-card height="700" width="700">
      <div class="buttons">
        <div class="plus-button">
          <v-btn class="mx-2" fab dark large color="purple" @click="counterplus">
            <p> {{ counter }} </p>
          </v-btn>
        </div>
        <div class="other-options">
          <v-btn class="mx-2" fab dark color="indigo">
            <v-icon dark> mdi-content-save-all </v-icon>
          </v-btn>
          <v-btn class="mx-2" fab dark color="indigo" @click="counterminus">
            <v-icon dark> mdi-minus </v-icon>
          </v-btn>
        </div>
      </div>
//      <OverlayButtonForCalendar />
    </v-card>
  </v-app>
</template>

<script>

//import OverlayButtonForCalendar from "./components/OverlayButtonForCalendar.vue"
//import { mdiContentSaveAll } from '@mdi/js'

export default {
  name: 'App',

  components: {
  //  OverlayButtonForCalendar
  },

  data: () => ({
    counter: 0
  }),
  methods: {
    counterplus(){
      console.log(this.counter)
      this.counter += 1
    },
    counterminus(){
      if (this.counter > 0){
        console.log(this.counter)
        this.counter -= 1
      } else {
        this.counter = 0
      }
    }
  },
};
</script>

<style scoped>
.template .v-app {
  display: flex;
  justify-content: center;
}

.buttons {
  display: flex;
  justify-content: center;
  margin-bottom: 50px;
  margin-top: 50px;
}

.other-options {
  display: flex;
  flex-direction: column;
}

.other-options button {
  margin: 10px 0 ;
}

.buttons .plus-button .mx-2 {
  display: flex;
  width: 300px;
  height: 300px;
}

.mx-2 p {
  font-size: 50px;
}
</style>
