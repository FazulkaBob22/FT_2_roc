<script setup>
import {ref, computed} from 'vue'
const cislo = ref(1)
const cislo2 = ref(0)
const cislo3 = ref(0)
const cislo4 = ref(0)
const cislo5 = ref(0)
const mojstring = ref('You are not prepared')

function krat5(){
  cislo.value = cislo.value *5
}
function deleno5(){
  cislo.value = cislo.value /5
}

function inc1(){
  cislo2.value = cislo2.value + 1
}
function dec1(){
  cislo2.value = cislo2.value - 1
}

function inc2(){
  cislo3.value = cislo3.value + 1
}
function dec2(){
  cislo3.value = cislo3.value - 1
}
function res2(){
  cislo3.value = 0
}

function inc3(){
  cislo4.value = cislo4.value + 1
}
function dec3(){
  cislo4.value = cislo4.value - 1
}
function res3(){
  cislo4.value = 0
}



const dajclass = computed(()=> {
  if (cislo.value > 5) {
    return 'red'
  }
  return 'green'

  
})

const Klas = computed(()=> {
  if (cislo2.value > 0){
    return 'greenb'
  }
  if (cislo2.value < 0){
    return 'redb'
  }
   
})
const Klas2 = computed(()=> {
  if (cislo3.value > 0){
    return 'greenb'
  }
  if (cislo3.value < 0){
    return 'redb'
  }
  if (cislo3.value == 0){
    return 'grayb'
  }
})


const Klas3 = computed(()=> {
  if (cislo4.value > 0){
    return 'greenb'
  }
  if (cislo4.value < 0){
    return 'redb'
  }
  if (cislo4.value == 0){
    return 'grayb'
  }
})


const Mocnina = computed(() => {
  return cislo4.value * cislo4.value
})

const Mocnina2 = computed(() => {
  return cislo5.value * cislo5.value
})

const Klas5 = computed(()=> {
  if (cislo5.value > 0){
    return 'greenb'
  }
  if (cislo5.value < 0){
    return 'redb'
  }
  if (cislo5.value == 0){
    return 'grayb'
  }
})

function inc5(){
  cislo5.value = cislo5.value + 1
}
function dec5(){
  cislo5.value = cislo5.value - 1
}
function res5(){
  cislo5.value = 0
}

</script>

<template>
  <div class="container">
  <div>
    <h1>inspo</h1>
    <p>{{ mojstring }}</p>
    <h3 :class="dajclass">{{ cislo }}</h3>

    <button @click="krat5">Krát 5</button>
    <button @click="deleno5">Deleno 5</button>
  </div>

  <div>
    <h1>uloha 1</h1>
    <h2 :class="Klas">{{ cislo2 }}</h2>

    <button @click="inc1">Increment</button>
    <button @click="dec1">Decrement</button>
  </div>


  <div>
    <h1>uloha 2</h1>
    <h2 :class="Klas2">{{ cislo3 }}</h2>

    <button @click="inc2">Increment</button>
    <button @click="dec2">Decrement</button>
    <button @click="res2">Reset</button>

  </div>

  <div>
    <h1>uloha 3</h1>
    <h2 :class="Klas3">{{ cislo4 }}</h2>
    <p>Druhá mocnina: {{ Mocnina}}</p>

    <button @click="inc3">Increment</button>
    <button @click="dec3">Decrement</button>
    <button @click="res3">Reset</button>

  </div>

  <div>
    <h1>uloha 4</h1>
    <h2 :class="Klas5">{{ cislo5 }}</h2>
    <p>Druhá mocnina: {{ Mocnina2 }}</p>

    <button @click="inc5" :class="{hidden: cislo5 > 5}">Increment</button>
    <button @click="dec5" :class="{hidden: cislo5 < -5}">Decrement</button>
    <button @click="res5">Reset</button>
  </div>
  </div>
</template>

<style scoped>
.red {
  color: red;
}
.green {
  color: green;
}
.redb {
  background-color: red;
}
.greenb {
  background-color: green;
}
.grayb {
  background-color: gray;
}
.container {
  display: flex;
  flex-direction: column;
}
.hidden {
  display: none;
}
</style>
