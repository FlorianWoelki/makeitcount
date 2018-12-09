<template>
  <div class="home text-xs-center">
    <h1 class="subheading mb-4">Select your bithday!</h1>

    <v-date-picker
      v-model="picker"
      :landscape="true"
      :reactive="true"
    ></v-date-picker>
  </div>
</template>

<script>
export default {
  data() {
    return {
      picker: new Date().toISOString().substr(0, 10)
    }
  }
}
</script>

