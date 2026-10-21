<script setup>
import {ref} from 'vue'
const name = ref()
const grade = ref()
const items = ref([{
name: "Ďuso",
 vek: 22,
},
{
 name: "Peťo",
 vek: 31,
}, {

 name: "Fero",
 vek: 14,
}])

const Students = ref([{
  name: "Janko",
  grade: 80,
},
{
  name: "Risko",
  grade: 67,
},
{
  name: "Andrejko",
  grade: 90,
}
])

function vymazElement(index) {
 items.value.splice(index, 1)
}
function vymazStudent(index) {
  Students.value.splice(index,1)
}
function pridajStudent(){
if(grade.value > 100 || grade.value < 0){
       alert("zly rozsah cisel"); 
       return;}


  Students.value.push({
    
    name: name.value,
    grade: grade.value
})
}
</script>

<template>
  
<div>
 <li v-for="item, index of items" :key="item.name + item.vek">{{ item.name }}>
  
  <input></input>
  
  <button @click="vymazElement(index)">Vymaz</button>
 </li> 
 </div><br>


 <div>
  <li v-if="Students.length > 0" v-for="student, index of Students" :key="student.name + student.grade">
    {{ student.name }} - {{ student.grade }}
    
    <button @click="vymazStudent(index)">DELETE</button>
  </li>
  <p v-else>NIC tu neni</p>
<input v-model="name" placeholder="meno..."></input>
    <input v-model="grade" placeholder="znamka..."></input>
    <button @click="pridajStudent()">pridaj</button>

 </div>


</template>

<style scoped>

</style>
