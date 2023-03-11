<template>
  <div class="home">
    <div class="home__hero">
      <p class="home__hero__paragraph">Ernesto Colon</p>
      <h1>Engineer</h1> 
      <span class="home__hero__separation">&</span> 
      <h1>Photographer</h1>
    </div>
    <div class="home__hero__footer">
      <div class="home__hero__footer__left">
        <span class="home__arrow">
          <img src="../assets/arrow.svg" alt="keep scrolling arrow"/>
          <img src="../assets/arrow.svg" alt="keep scrolling arrow"/>
        </span>
        <p>
          <span>Keep</span>
          <span>Scrolling</span>
        </p>
      </div>
      <div class="home__hero__footer__right">
        <p>LinkedIn</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.home__hero {
  display: flex;
  flex-direction: column;
  justify-content: center
}

.home__hero__paragraph {
  color: var(--vt-c-orange);
  font-size: x-large;
  text-transform: uppercase;
  line-height: 1.5;
  display: inline-block;
  font-family: "ClashDisplaySemiBold", sans-serif;
}

.home__hero h1 {
  font-size: clamp(5rem,20vh,16vw);
  text-align: center;
  font-family: "ClashDisplayBold", sans-serif;
}

.home__hero__separation{
  font-family: "ClashDisplay", sans-serif;
  font-size: clamp(3rem,9vh,10vw);
  text-align: center;
}

.home__hero__footer{
  display: flex;
  justify-content: space-between;
  padding-top: 5rem;
}

.home__hero__footer__left{
  align-items: center;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  height: 3.5rem;
  overflow: hidden;
  opacity: .6;
}

.home__arrow {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transform: translateY(-30%);
  animation: infiniteArrow 2s cubic-bezier(.175,.885,.32,1) infinite;
}

.home__arrow img:last-child {
  margin-top: 0.3rem;
}

.home__hero__footer__left img {
  height: 2.8rem;
  width: 2rem
}

.home__hero__footer__left p span {
  display: block;
  margin-bottom: 0.5rem;
}

@keyframes infiniteArrow {
  0% {
    transform: translateY(-30%)
  }

  to {
    transform: translateY(30%)
  }
}
</style>