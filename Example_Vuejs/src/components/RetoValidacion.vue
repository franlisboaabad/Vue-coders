<template>
    <div>
        <h1>🧠 RETO: Formulario de usuario con validación</h1>
        <div>
            <form>
                <input v-model="nombre" placeholder="Escribe tu nombre"> <br> <br>
                <input v-model="edad" placeholder="Escribe tu edad"> <br> <br>

                <p v-if="edad >= 18">✅ "Bienvenido, {{ nombreMayuscula }}. Puedes continuar"</p>
                <p v-else-if="edad > 0">⚠️ "Lo sentimos, debes ser mayor de edad."</p>

            </form>
        </div>
    </div>
</template>

<style>
form {
    padding: 20px;
    border: 1px solid;
}
</style>

<script setup>
import { ref, computed, watch } from "vue";
const nombre = ref('')
const edad = ref(0)

const nombreMayuscula = computed(() => nombre.value.toUpperCase())

watch(nombre, (nuevo, anterior) => {
    console.log(`Nombre cambio de: ${anterior} a ${nuevo}`);

})


watch(edad, (nuevo, anterior) => {
    console.log(`Edad cambio de :${anterior} a ${nuevo}`);
})



</script>