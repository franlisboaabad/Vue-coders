<template>
    <div>
        <input v-model="mensaje" placeholder="Escribe tu mensaje">
        <button @click="enviarMensaje">Enviar</button>
    </div>
</template>

<script setup>
import { ref, reactive } from "vue";

const mensaje = ref('')

function enviarMensaje() {
    alert(`Enviando mensaje: ${mensaje.value}`);
}

</script>