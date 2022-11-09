<template>
  <q-page class="q-pa-md">
    <q-btn color="primary" :label="counter" size="xl" class="full-width q-mb-md" @click="increaseCounter"/>
    <div class="row">
    <div class="col text-left">
      <q-btn flat round color="negative" icon="remove" size="lg" @click="decreaseCounter"/>
    </div>
    <div class="col text-center">
      <q-btn flat round icon="restart_alt" size="lg" @click="resetCounter"/>
    </div>
    <div class="col text-right">
      <q-btn flat round color="positive" icon="add" size="lg" @click="increaseCounter"/>
    </div>
  </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

let counter = ref(0)

const increaseCounter = () =>{
  counter.value++
}

const decreaseCounter = () =>{
  counter.value--
}

const resetCounter = () =>{
  counter.value = 0
}
</script>
