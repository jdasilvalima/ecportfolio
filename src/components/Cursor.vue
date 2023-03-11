<template>
  <div ref="cursor" class="cursor">
    <div class="colorOne"></div>
    <div class="colorTwo"></div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const cursor = ref<HTMLInputElement>();

function updateMousePosition(event: MouseEvent) {
  if (!cursor.value) return;

  cursor.value.style.left = event.pageX + 'px';
  cursor.value.style.top = event.pageY + 'px';
}

onMounted(() => {
  window.addEventListener('mousemove', updateMousePosition);
})

onUnmounted(() => {
  window.removeEventListener('mousemove', updateMousePosition);
})
</script>

<style scoped>
.cursor {
  pointer-events: none;
  position: fixed;
  left: 0;
  top: 0;
  opacity: .85;
  height: 1rem;
  width: 1rem;
  z-index: -1;
}

.cursor div {
  width: 13rem;
  height: 13rem;
}

.cursor div:nth-child(1) {
  top: calc(50% - 15rem);
  left: calc(50% - 15rem)
}

.cursor div:nth-child(2) {
  top: calc(37% - 22rem);
  left: calc(35% - 22rem)
}

.cursor div:nth-child(3) {
  top: calc(68% - 22rem);
  left: calc(45% - 22rem)
}

.colorOne {
  animation: 10s colorOne linear infinite;
  background: linear-gradient(90deg,#00bac7 1.98%,#00bac7 1.99%,#0c6f90 100%);
  opacity: .8;
  filter: blur(127px)
}

.colorTwo {
  animation: colorTwo 6s linear infinite;
  background: linear-gradient(90deg,#046dde 1.98%,#046dde  1.99%,#0c6f90 100%);
  opacity: .8;
  filter: blur(127px)
}

@keyframes colorOne {
  0% {
      transform: rotate(0) translate(-40px) rotate(0) scale(1)
  }

  50% {
      transform: rotate(-180deg) translate(-40px) rotate(-180deg) scaleY(1.33)
  }

  to {
      transform: rotate(-360deg) translate(-40px) rotate(-360deg) scale(1)
  }
}

@keyframes colorTwo {
  0% {
      transform: rotate(0) translate(30px) rotate(0) scale(1)
  }

  33% {
      transform: rotate(180deg) translate(30px) rotate(-180deg) scaleX(1.66)
  }

  to {
      transform: rotate(360deg) translate(30px) rotate(-360deg) scale(1)
  }
}
</style>
