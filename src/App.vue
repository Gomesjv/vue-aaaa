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
   function maismil (){
    contador.value = contador.value + 1000
   }

function milao (){
  contador.value = contador.value + 1000000000000000000
}

onMounted (() =>{
  console.log(`${contador.value}`)
})
const mensagem = '<span style="color: red">Deve ser vermelho.</span>'
const mensagemv = '<span style="color: green">Deve ser vermelho.</span>'
</script>

<template>
 <button @click = "incrementar">+</button>
  <button @click="decrementar">-</button>
<button @click="reset">C</button>
<button @click="maismil">1000</button>
<button @click="milao">aaa</button>
  <p>valor do contador : {{ contador }}</p>
  <div v-if= "contador >= 10 " v-html="mensagem" ></div>
  <div v-else v-html="mensagemv" ></div>
</template>

<style>
button{
  width: 50px;
  height: 30px;
  border-radius: 20%;
  color: white;
  background-color: black;
}
</style>
