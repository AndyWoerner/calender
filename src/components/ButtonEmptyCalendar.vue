<template>
    <button 
        class="btn btn-danger btn-block"
        @click="emptyCalendar"
        >
        <i class="fas fa-eraser"></i> Alle Termine löschen
    </button>
</template>

<script>
import {store} from "../store"

export default {
    name: "ButtonEmptyCalendar",
    methods: {
        emptyCalendar(){
            store.emptyCalendar()
        }
    }
}
</script>