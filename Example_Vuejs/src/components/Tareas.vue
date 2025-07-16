<template>
    <div>
        <h1>Lista de Tareas</h1>
        <input v-model="nuevaTarea" placeholder="Ingrese su tarea">
        <button @click="AddTarea">Agregar Tarea</button>

        <ul>
            <li v-for="(item, index) in tareas" :key="index">{{ item }}</li>
        </ul>
    </div>
</template>


<script setup>
import { ref, computed, watch } from "vue";
const nuevaTarea = ref('')
const tareas = ref([])

function AddTarea() {
    if (nuevaTarea.value.trim()) {
        tareas.value.push(nuevaTarea.value.trim())
        nuevaTarea.value = ''
    }
}

</script>