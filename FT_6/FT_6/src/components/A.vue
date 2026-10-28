<script setup>
const props = defineProps({
    cislo: Number
})
import {ref} from 'vue'
</script>

<template>
    <h1>Komponent a: {{ props.cislo }}</h1>

</template>

