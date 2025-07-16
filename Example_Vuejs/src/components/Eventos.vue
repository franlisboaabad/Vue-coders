<template>
    <div>
        <p>Contador {{ contador }}</p>
        <button @click="contador++">Aumentar +1</button>
        <button @click="contador += 10">Aumentar +10</button>
        <button @click="Reset">Reset</button>
    </div>
</template>


<script setup>
import { ref } from "vue";
const contador = ref(0)

function Reset() {
    contador.value = 0
}

</script>