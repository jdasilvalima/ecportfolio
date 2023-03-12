<template>
  <main class="home">
    <Header/>
    <Description/>
    <Works/>
  </main>
</template>

<script setup lang="ts">
import Header from '../components/Header.vue'
import Description from '../components/Description.vue'
import Works from '../components/Works.vue'
</script>

<style>
  .home{
    padding-top: 4rem;
  }
</style>
