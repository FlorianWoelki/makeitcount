<template>
  <div class="dashboard text-xs-center">
    <h1 class="subheading mb-4">Welcome to the Dashboard!</h1>
    <p>{{ this.pickedDate }}</p>
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
