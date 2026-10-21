<script setup>
import {ref} from 'vue'
const props = defineProps(['title','body'])

const emit = defineEmits(['enlarge-text'])

</script>
<template>
    <h1>{{props.title}}</h1><br>
    <p>{{ props.body }}</p><br>
    
</template>