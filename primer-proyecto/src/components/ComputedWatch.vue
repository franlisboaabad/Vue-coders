<template>
    <div>
        <input v-model="nombre" placeholder="Nombre" />
        <input v-model="apellido" placeholder="Apellido" />
        <p>Nombre completo (computed): {{ nombreCompleto }}</p>
    </div>
</template>

<script setup>
import { ref, reactive, computed, watch } from "vue";

const nombre = ref('')
const apellido = ref('')


const nombreCompleto = computed(() => {
    return `${nombre.value} ${apellido.value}`.trim()
})

watch(nombreCompleto, (nuevoValor, anterior) => {
    console.log(`Nombre completo cambio: ${anterior} a ${nuevoValor}`);

})

</script>