<template>
    <div>
        <p>Mi primer compnente usando V-Model</p>
        <h2>Hola {{ nombre }}</h2>
        <input v-model="nombre" placeholder="Escribe tu nombre" />
        <h3>Tus apellidos {{ apellidos }} </h3>
        <input v-model="apellidos" placeholder="Escribe tus Apellidos">
    </div>
</template>

<script setup>
import { ref } from 'vue'
const nombre = ref('Mundo')
const apellidos = ref('')
</script>

<style scoped>
h2 {
    color: #42b983;
}
</style>
