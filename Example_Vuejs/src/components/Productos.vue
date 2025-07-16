<template>
    <div>
        <ul>
            <li v-for="(item, index) in productos" :key="index">
                {{ item.id }} - {{ item.nombre }} - <span v-if="item.stock <= 0">sin stock</span> <span
                    v-else="item.stock > 0 ">{{ item.stock }}</span>
            </li>
        </ul>
    </div>
</template>

<script setup>
import { ref, computed, watch } from "vue";

const productos = ref(
    [
        { id: 1, nombre: "Laptop Lenovo ThinkPad", stock: 12 },
        { id: 2, nombre: "Mouse inalámbrico Logitech", stock: 0 },
        { id: 3, nombre: "Teclado mecánico Redragon", stock: 18 },
        { id: 4, nombre: "Monitor LG 24”", stock: 10 },
        { id: 5, nombre: "Memoria USB 32GB Kingston", stock: 50 },
        { id: 6, nombre: "Disco Duro Externo 1TB WD", stock: 8 },
        { id: 7, nombre: "Smartphone Samsung A54", stock: 22 },
        { id: 8, nombre: "Tablet Xiaomi Pad 6", stock: 15 },
        { id: 9, nombre: "Auriculares Sony WH-CH520", stock: 14 },
        { id: 10, nombre: "Silla ergonómica oficina", stock: 9 },
        { id: 11, nombre: "Cámara Web Logitech C920", stock: 7 },
        { id: 12, nombre: "Impresora HP DeskJet 2720", stock: 6 },
        { id: 13, nombre: "Cable HDMI 2m", stock: 60 },
        { id: 14, nombre: "Hub USB 4 Puertos", stock: 25 },
        { id: 15, nombre: "Power Bank 10,000mAh Xiaomi", stock: 30 },
        { id: 16, nombre: "Parlante Bluetooth JBL Go 3", stock: 20 },
        { id: 17, nombre: "Router TP-Link AC1200", stock: 11 },
        { id: 18, nombre: "Mochila para laptop", stock: 40 },
        { id: 19, nombre: "Licencia Windows 11 Pro", stock: 5 },
        { id: 20, nombre: "Soporte monitor ajustable", stock: 13 }
    ]
)



</script>