<template>
  <div class="dashboard text-xs-center">
    <h1 class="subheading mb-4">Welcome to the Dashboard!</h1>
    <p>{{ this.pickedDate }}</p>

    <ul class="weeks-title">
      <li></li>
      <li
        v-for="i in 52"
        :key="'weeks-title-' + i"
      >{{i}}</li>
    </ul>
    <ul
      class="weeks-boxes"
      v-for="i in 81"
      :key="'weeks-boxes-' + i"
    >
      <li>{{i - 1}}</li>
      <li
        v-for="j in 52"
        :key="'weeks-boxes-line-' + j"
      >{{j}}</li>
    </ul>
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
.weeks-title {
  font-size: 10px;
  color: #777;
}
.weeks-title li {
  margin: 1px;
  display: inline-block;
  width: 1.6%;
  color: #666;
  text-align: center;
}

.weeks-boxes {
  font-size: 12px;
  color: #777;
}
.weeks-boxes li:first-child {
  border-style: none;
}
.weeks-boxes li {
  margin: 1px;
  list-style-type: none;
  display: inline-block;
  width: 1.6%;
  border-style: solid;
  border-width: 1px;
  text-align: center;
  margin-bottom: 1px;
}
</style>

