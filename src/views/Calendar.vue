<template>
  <div class="calendar">
    <h1>This is where the calendar componet will show</h1>
    <br>
    <br>
    <calendarComponent />
  </div>
</template>

<script>
import calendarComponent from '/Users/suraj/Documents/Personal Projects/foodCalendar--Vuejs-BootstrapVue/src/components/calendarComponent.vue'

export default {
  name: 'calendar',
  components: {
      calendarComponent
  }
}
</script>