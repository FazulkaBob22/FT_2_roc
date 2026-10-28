<script setup>
import A from './components/A.vue'
import B from './components/B.vue'
import { computed, ref , watch} from 'vue'

const vstup = ref("")
const ret = computed(() => String(vstup.value).length)

watch(vstup, (hodnota) => {
  if (hodnota<0) vstup.value = 0
  else if (hodnota > 100) vstup.value = 100
})
</script>

<template>
  <div>
  <input type="number" v-model="vstup">
 <A :cislo="vstup"></A>
<B :vstub="ret"></B></div>
</template>

<style scoped>

</style>
