<script setup>
import { reactive, ref } from 'vue'

const awesome = ref(true) 
const count = ref(0)
const text = ref('')


function increment(){
  count.value++
}

function token() {
  awesome.value = !awesome.value
}


</script>

<template>
  <input v-model="text" placeholder="type here">
    <p>{{ text }}</p>
      <button @click="token">toggle</button>
      <button @click="increment">token: {{ count }}</button>
    <h1 v-if="awesome">wahhh saya pintar</h1>
    <h1 v-else>ohh noo saya tidak pintar</h1>
</template>