<template>
  <div class="dashboard text-xs-center">
    <h1 class="subheading mb-4">Welcome to the Dashboard!</h1>
    <p>{{ this.pickedDate }}</p>

    <WeekCalendar />
  </div>
</template>

<script>
import WeekCalendar from '@/components/WeekCalendar'

export default {
  name: 'Dashboard',
  components: { WeekCalendar },
  props: {
    pickedDate: {
      type: String,
      required: true
    }
  }
}
</script>
