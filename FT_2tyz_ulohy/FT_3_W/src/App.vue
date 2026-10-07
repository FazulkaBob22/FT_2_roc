<script setup>
import {ref} from 'vue';
import { onMounted } from 'vue';

const cislo = ref(0);
const markdowntext = ref('');
const text = ref('');


onMounted(() => {
  randomC();
});

function randomC(){
  cislo.value = Math.floor(Math.random() * 100) + 1; 
}

function ulozDoPremennej(event) {
  markdowntext.value = event.target.value;
}

const dlzka = () => {
  if (text.value.length > 10){
    return true
  }
  else {
    return false
  }
}



</script>

<template>
  <h1> cislo: {{ cislo }}</h1><br>

  <textarea @keyup.enter="ulozDoPremennej"></textarea><br>
  <div v-html="markdowntext"></div>
  <br>
  <textarea v-model="text" :disabled="dlzka()"></textarea><br>
  <div>
  <button @click="Vymaz">vymaz</button></div><br><br>


  <textarea ></textarea><br>
  <input type="number">
  <input type="number">


</template>

<style scoped>

</style>
