<script setup>
import {ref} from 'vue'

    const titles = ref([
        {title: 'Placeholder name 1', image: '/images/obrazok1.jpg'},
        {title: 'Placeholder name 2', image: '/images/obrazok2.jpg'},
        {title: 'Placeholder name 3', image: '/images/obrazok3.jpg'}
    ])
</script>

<template>

    <div v-for="value in titles" :key="value.title" class="item">
        <img :src="value.image" :alt="value.title">
        <h5>{{ value.title }}</h5>

    </div>
    
</template>

<style scoped>
.item {
  display: flex;
  align-items: center;
  gap: 20px;
}

.item img {
  width: 150px;
  height: auto;
}
</style>