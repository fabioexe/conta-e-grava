<template>
  <v-row justify="center">
    <v-btn class="white--text btn-abrir" color="teal" @click="overlay = !overlay">
      Abrir Calendário
    </v-btn>

    <v-overlay :value="overlay">
        <Calendar class="calendar"/>
      <v-btn class="white--text btn-fechar" color="teal" @click="overlay = false">
        Fechar Calendário
      </v-btn>
    </v-overlay>
  </v-row>
</template>

<script>

import Calendar from "../components/Calendar.vue"

  export default {
    
    components: { Calendar },  

    data: () => ({
      overlay: false,
    }),
  }
</script>

<style>
.v-overlay{
    display: flex;
}

.calendar {
    width: 100%;
    height: 100%;
}

.v-calendar-weekly__day {
    width: 100px;
}

</style>