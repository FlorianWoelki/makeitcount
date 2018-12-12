<template>
  <div class="dashboard text-xs-center">
    <h1 class="subheading mb-4">Welcome to the Dashboard!</h1>
    <p>{{ this.pickedDate }}</p>

    <div class="weeks">
      <span
        v-for="i in 52"
        :key=i
      >{{i}} </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Dashboard',
  props: {
    pickedDate: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
.weeks span {
  font-size: 12px;
  font-weight: 300;
}
</style>

