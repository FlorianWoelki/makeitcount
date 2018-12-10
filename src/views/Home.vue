<template>
  <div class="home text-xs-center">
    <h1 class="subheading mb-4">Select your bithday!</h1>

    <v-flex xs12>
      <v-date-picker
        v-model="picker"
        max="2019"
        :landscape="true"
        :reactive="true"
      ></v-date-picker>
    </v-flex>
    <v-flex xs12>
      <v-btn
        large
        outline
        color="info"
        class="mb-4 my-4"
        v-on:click="goToDashboard"
      >Continue</v-btn>
    </v-flex>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      picker: new Date().toISOString().substr(0, 10)
    }
  },
  methods: {
    goToDashboard: function() {
      this.$router.push({ name: "dashboard", params: { pickedDate: this.picker } });
    }
  }
}
</script>

