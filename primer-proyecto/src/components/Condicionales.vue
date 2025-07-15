<template>
    <div>
        <p>Condicionales</p>
        <h1>Hola: {{ nombre }} - {{ apellidos }}</h1>
        <input type="text" placeholder="Escribe tu edad" v-model="edad">

        <p v-if="edad >= 18">Eres Mayor de Edad</p>
        <p v-else>Eres Menor de Edad</p>

        <p>Mis Frutas</p>
        <ul>
            <li v-for="(item, index) in frutas" :key="index">{{ item }}</li>
        </ul>

    </div>
</template>

<script setup>
import { ref } from "vue";
const nombre = ref('Frank')
const apellidos = ref('Lisboa Abad')
const edad = ref(0)
const frutas = ref(['Manzana', 'Platano', 'Pera', 'Mango', 'Limon'])

</script>