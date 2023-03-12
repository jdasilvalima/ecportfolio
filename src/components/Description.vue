<template>
  <div class="home__description">
    <div class="description__paragraphs">
      <p>Hi, I am Ernesto !</p>
      <p>I am a engineer who constantly seeks for 
        innovative solutions to everyday problems.</p>
      <p>For whatever reason it is you are here, welcome.</p>
    </div>
    <a href="/about" class="link link__metis">About me</a>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.home__description {
  padding-top: 5rem;
  display: grid;
  place-content: center;
  height: 100vh;
  max-height: 80rem;
  width: min(100%,35rem);
  margin: auto;
}

.home__description p {
  font-size: 2.0rem;
  line-height: 1.5;
  padding-bottom: 1.5rem;
  letter-spacing: 1px;
}

.home__description a {
  font-size: 2.5rem;
  width: fit-content;
  margin-top: 1.5rem;
  font-family: "ClashDisplayBold", sans-serif;
}
</style>