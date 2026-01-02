<script setup>
import { ref } from 'vue'

const celcius = ref(0)
const fahrenheit = ref(32)

function onCelcius(e) {
    celcius.value = e.target.value
    fahrenheit.value = celcius.value * 1.8 + 32
}

function onFahrenheit(e) {
    fahrenheit.value = e.target.value
    celcius.value = (fahrenheit.value - 32) / 1.8
}
</script>

<template>
    <input type="number" :value="celcius" @change="onCelcius">
    Celcius =
    <input type="number" :value="fahrenheit" @change="onFahrenheit">
    Fahrenheit
</template>