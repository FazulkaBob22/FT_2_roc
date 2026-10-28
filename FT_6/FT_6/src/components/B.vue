<script setup>
import A from './A.vue'
import {ref} from 'vue'

const props = defineProps(['vstub'])
const vstub = ref(0)
</script>

<template>
<h1>Komponent B: Cifry:{{ props.vstub }}

</h1>

</template>

<style scoped>

</style>