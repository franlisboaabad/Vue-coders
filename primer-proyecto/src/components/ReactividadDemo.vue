<template>
    <div>
        <h2>Contador: {{ contador }}</h2>
        <button @click="contador++">Aumentar</button>
        <hr>

        <p>Datos personales</p>
        <p>Nombre:{{ persona.nombre }} - Apellidos: {{ persona.apellidos }} - Edad:{{ persona.edad }}</p>
        <input v-model="persona.nombre" placeholder="Escribe tu nombre">
        <input v-model="persona.apellidos" placeholder="Escribe tu apellidos">
        <input v-model="persona.edad" placeholder="Escribe tu edad">


    </div>
</template>


<script setup>
import { ref, reactive } from "vue";
const contador = ref(0);

const persona = reactive({
    nombre: 'Juan',
    apellidos: 'Pérez',
    edad: 30,
    correo: 'juan.perez@example.com',
    direccion: {
        calle: 'Calle Falsa 123',
        ciudad: 'Ciudad de México',
        pais: 'México'
    },
    intereses: ['leer', 'viajar', 'programar']
});


</script>