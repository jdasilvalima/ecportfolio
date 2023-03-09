<template>
  <div class="page">
    <Navbar/>
    <RouterView/>
    <Cursor/>
  </div>
</template>

<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import Cursor from './components/Cursor.vue'
</script>

<style scoped>

</style>
