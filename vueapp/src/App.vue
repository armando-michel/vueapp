<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h1>Boton de Colores</h1>
  <button @click="color='red'" style="color:red">Rojo</button>
  <button @click="color='blue'" style="color:blue">Azul</button>
  <button @click="color='green'" style="color:green">Verde</button>
  <h2>{{valor}}</h2>
  <button @click="incrementar">+</button>
  <button @click="decrementar">-</button> 
</template>


<script setup>
import { ref } from "@vue/reactivity";
const valor = ref(0)
const color = ref("red")
let incrementar = () =>  valor.value ++
let decrementar = () =>  valor.value --



// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  color: v-bind(color)
}



</style>
