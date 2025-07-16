<template>
    <div>
        <input type="number" v-model="numero1" placeholder="Ingrese el primer numero">
        <input type="number" v-model="numero2" placeholder="Ingrese el segundo numero">

        <p>La suma es : {{ sumaNumeros }}</p>
    </div>
</template>

<script setup>
import { ref, computed, watch } from "vue";

const numero1 = ref(0);
const numero2 = ref(0);


const sumaNumeros = computed(() => numero1.value + numero2.value)

watch([numero1, numero2], ([nuevo1, nuevo2]) => {
    console.log(`num1 cambió a ${nuevo1}, num2 a ${nuevo2}`)
})

</script>