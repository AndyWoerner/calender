<template>
  <div id="calendar-entry">
    <div class="container mt-5">
      <div class="row">
        <div class="col-6 offset-3">
          <div class="card">
            <div class="card-header text-center bg-vue">
              <h5>
                Neuer Termin für:
                <strong>{{ getNameOfActiveDay }}</strong>
              </h5>
            </div>
            <div class="card-body">
                <div 
                    class="alert alert-danger"
                    v-show="error"
                >
                    Der Titel darf nicht leer sein.
                </div>
              <input
                type="text"
                class="form-control"
                placeholder="Neuer Termin"
                v-model="eventTitle"
              />
              <div class="mt-3 text-center">
                <span
                  v-for="(color, index) in ['primary', 'success', 'info', 'warning', 'danger']"
                  :key="index"
                  class="alert mr-2 square"
                  :class="[eventColor === color ? getBorderColor : '','alert-'+color]"
                  style="cursor: pointer"
                  @click="changeEventColor(color)"
                ></span>
              </div>
              <hr />
              <button
                class="btn bg-vue2 btn-block"
                @click="storeEvent(eventTitle, eventColor)"
              >Eintragen</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { store } from "../store";

export default {
  name: "CalendarEntry",
  data() {
    return {
      eventColor: "primary",
      eventTitle: "",
      error: false
    };
  },
  computed: {
    getBorderColor() {
      return "border border-" + this.eventColor;
    },
    getNameOfActiveDay() {
      return store.getActiveDay().fullName;
    }
  },
  methods: {
    changeEventColor: function(color) {
      this.eventColor = color;
    },
    storeEvent(eventTitle, eventColor) {
        if (eventTitle  === "") return this.error = true
      store.storeEvent(eventTitle, eventColor);
      this.eventTitle = "";
      this.eventColor = "primary";
      this.error = false
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
.square {
  width: 40px;
  height: 40px;
}
</style>