<script setup>
import { ref, onMounted } from 'vue';

const contador = ref(0)

function incrementar (){
  contador.value++
}

  function decrementar (){
    if(contador.value > 0){
      contador.value--
    }
   
}
function reset (){
    contador.value = 0
   }

onMounted (() =>{
  console.log(`${contador.value}`)
})
</script>

<template>
 <button @click = "incrementar">+</button>
  <button @click="decrementar">-</button>
<button @click="reset">C</button>
  <p>valor do contador : {{ contador }}</p>
</template>

<style>
button{
  width: 30px;
  height: 30px;
  border-radius: 20%;
  color: white;
  background-color: black;
}

</style>
