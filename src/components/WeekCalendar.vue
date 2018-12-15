<template>
  <div class="week-calendar">
    <ul class="horizontal-lines">
      <li></li>
      <li
        v-for="i in 52"
        :key="'title-' + i"
      >{{i}}</li>
    </ul>
    <ul
      class="boxes"
      v-for="i in 81"
      :key="'boxes-' + i"
    >
      <li>{{i - 1}}</li>
      <li
        v-for="j in 52"
        :key="'boxes-line-' + j"
      >{{j}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'WeekCalendar'
}
</script>


<style>
.week-calendar .horizontal-lines {
  font-size: 10px;
  color: #777;
}
.week-calendar .horizontal-lines li {
  margin: 1px;
  display: inline-block;
  width: 1.6%;
  color: #666;
  text-align: center;
}

.week-calendar .boxes {
  font-size: 12px;
  color: #777;
}
.week-calendar .boxes li:first-child {
  border-style: none;
}
.week-calendar .boxes li {
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
