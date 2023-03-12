<template>
  <div class="home__works">
    <p>04</p>
    <h2>Featured 
      <br/>
      Projects
    </h2>
    <div class="home__works__contents">
      <article>
        <span class="home__works__date">01/04</span>
        <a class="home__works__content" href="/">
          <div class="monochrome"></div>
          <div class="home__works__main">
            <p>Moniepoint
              <br/>
              Inc.
            </p>
          </div>
          <p class="home__works__content__year">2023</p>
          <img src="../assets/link.svg"/>
        </a>
      </article>
    </div>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.home__works {
  padding-top: 5rem;
}

.home__works p {
  font-weight: 700;
  position: absolute;
  right: 25rem;
  font-size: 1.5rem;
}

.home__works h2 {
  font-weight: 700;
  font-size: 7rem;
  text-align: center;
  font-family: "ClashDisplayBold", sans-serif;
}

.home__works__contents {
  align-items: center;
  display: flex;
  justify-content: center;
  flex-direction: column;
  gap: 10rem;
  margin-top: 9rem;
}

.home__works__contents article {
  position: relative;
  display: block;
  width: min(100%,40rem);
  height: 31rem;
  background-size: cover;
  background-position: center;
}

.home__works__contents article:nth-child(odd) {
  margin-left: auto;
}

.home__works__contents article>span {
  font-weight: 500;
  font-size: 3.2rem;
  position: absolute;
  top: 0;
}

.home__works__contents article:nth-child(odd)>span {
  left: -12rem;
}

article {
  background-image: url(https://images.prismic.io/folio2022/1352546f-bd02-4eff-b326-d30d6f9e888a_Screenshot+2023-02-01+at+15.18.39.webp?auto=compress,format);
  translate: none;
  rotate: none;
  scale: none;
  transform: perspective(800px);
  transform-origin: 50% 50%;
}

a {
  outline: none;
  text-decoration: none;
}

.home__works__content {
  position: relative;
  display: block;
  width: 100%;
  height: 100%;
  color: #fcf3ea;
}

.home__works__content .monochrome {
  z-index: 4;
  background: #fcf3ea;
  mix-blend-mode: color;
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}

.home__works__content:before,  .home__works__content:after, .home__works__content .monochrome {
  content: "";
  transition: opacity .4s cubic-bezier(.77,0,.175,1);
}
</style>