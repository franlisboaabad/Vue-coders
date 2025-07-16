<template lang="">
    <div>
        <input v-model="usuario.nombre" placeholder="Nombre" />
        <input v-model="usuario.email" placeholder="Email" />

        <p>Nombre: {{ usuario.nombre }}</p>
        <p>Email: {{ usuario.email }}</p>

    </div>
</template>


<script setup>
import { ref, reactive } from "vue";

const usuario = reactive({
    nombre: '',
    email: ''
})
</script>