<script setup>
import { ref } from 'vue'
import { motion } from 'motion-v'

const guessState = ref('none') // 'none', 'wrong', 'right'

const guessing = () => {
  guessState.value = 'wrong'
  setTimeout(() => {
    guessState.value = 'none'
  }, 1000)
}

const guessing2 = () => {
  guessState.value = 'right'
  setTimeout(() => {
    guessState.value = 'none'
  }, 1000)
}
</script>


<template>
  <motion.div class="test" :animate="{
    boxShadow: guessState === 'wrong'
      ? '3px 3px 19px -3px red'
      : guessState === 'right'
        ? '3px 3px 19px -3px green'
        : 'rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px'
  }" :transition="{ duration: 0.3 }">
    this is test div
  </motion.div>

  <button @click="guessing">guessing</button>
  <button @click="guessing2">guessing right</button>
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
