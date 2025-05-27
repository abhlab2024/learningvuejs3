<script setup>
import { ref } from 'vue'
import { motion } from 'motion-v'

const isGuessed = ref(false)

const guessing = () => {
  isGuessed.value = true
  setTimeout(() => {
    isGuessed.value = false
  }, 1000) // back to normal after 0.5s
}
</script>

<template>
  <motion.div class="test" :animate="{
    boxShadow: isGuessed
      ? '3px 3px 19px -3px red'
      : 'rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px'
  }" :transition="{ duration: 0.3 }">
    this is test div
  </motion.div>

  <button @click="guessing">guessing</button>
</template>

<style>
.test {
  border: 10px solid rgb(254, 255, 199);
  width: 400px;
  height: 300px;
  transition: box-shadow 0.3s ease;
  margin-left: 3rem;
  margin-top: 3rem;
}

button {
  margin-top: 4rem;
}
</style>
