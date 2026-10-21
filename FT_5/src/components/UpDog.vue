<script setup>
import {ref} from 'vue'
const props = defineProps(['image', 'title'])

</script>

<template>
    <h1>{{ props.title }}</h1>
</template>