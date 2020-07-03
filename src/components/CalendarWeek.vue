<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-12">
                <div class="card-group">
                    <CalendarDay 
                        v-for="day in state.calendarWeekData"
                        :key="day.id"
                        :day="day"
                    />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { store } from "../store";
import CalendarDay from "./CalendarDay"

export default {
    name: "CalendarWeek",
    // innerhalb einer Singel-File-Komponente muss das data-Attribut eine Funktion sein!
    data() {
        return {
            state: store.state,
        }
    },
    components: {
        CalendarDay
    }
}
</script>

<style scoped>
    
</style>
