<script setup>
import { useStorage } from '@/composables/useStorage'

let food = useStorage('food', 'pizza')
let age = useStorage('age', 30)
let obj = useStorage('obj', { one: 'one' })

setTimeout(() => {
  obj.value.one = 'CHANGED'
}, 3000)
</script>

<template>
  <main>
    <p>What is your favorite food? <input type="text" v-model="food" /></p>
    <p>What is your age? <input type="text" v-model="age" /></p>
  </main>
</template>
