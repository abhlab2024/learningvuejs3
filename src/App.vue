<script setup>
import { RouterLink, RouterView } from 'vue-router';
import { motion } from 'motion-v';
import testing from './components/testing.vue';
</script>

<template>


  <h1>Praise the LORD</h1>

  <div class="test">
    this is test div
  </div>


  <testing/>




  <!-- <RouterView /> -->
</template>


<style>

  .test {
    border: 1px solid black;
  }

</style>
