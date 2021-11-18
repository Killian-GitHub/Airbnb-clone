<template>
  <Datepicker v-model="date"></Datepicker>
</template>

// Revoir code 1:20

<script>
  import Datepicker from 'vue3-date-time-picker';
  import 'vue3-date-time-picker/dist/main.css'

  export default {
    components: {
      Datepicker
    },
  }
</script>