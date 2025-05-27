<script setup>
import { RouterLink, RouterView } from 'vue-router';
import { motion } from 'motion-v';
import testing from './components/testing.vue';



import { useMotionValue } from 'motion-v'

</script>

<template>

<div class="test">
  this is test div
</div>



</template>


<style>
.test {
  border: 10px solid rgb(254, 255, 199);
  width: 400px;
  height: 300px;
  box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;
}
</style>
