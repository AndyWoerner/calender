<template>
  <div class="card">
    <div
      class="card-header text-center"
      :class="[day.active ? activeClass : defaultClass]"
      style="cursor: pointer"
      @click="setActiveDay(day.id)"
    >
      <strong>{{day.fullName }}</strong>
    </div>
    <div 
        class="card-body"
        :class="[day.active ? activeBgClass : '']"
        >
      <div>{{ day.id }}</div>
      <CalendarEvent v-for="(event, index) in day.events" :key="index" :event="event" :day="day" />
    </div>
  </div>
</template>

<script>
import CalendarEvent from "./CalendarEvent";
import { store } from "../store";

export default {
  name: "CalendarDay",
  props: ["day"],
  data() {
      return {
          activeClass: "bg-vue2",
          defaultClass: "bg-vue",
          activeBgClass: "bg-color-vue2"
      }
  },
  components: {
    CalendarEvent
  },
  methods: {
    setActiveDay(dayId) {
      store.setActiveDay(dayId);
    }
  }
};
</script>

<style scoped>
.bg-vue {
  background-color: rgb(52, 73, 94);
  color: white;
} 
.bg-vue2 {
  background-color: rgb(65, 184, 131);
  color: white;
}
.bg-color-vue2 {
    background-color: rgb(65, 184, 131, 0.05);
}
</style>