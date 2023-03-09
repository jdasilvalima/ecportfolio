<template>
    <header>
      <div class="navigation__header">
        <span class="navigation__logo">
          <a href="/" aria-label="home-direction">E.C.</a>
        </span>

        <div class="navigation__toggle">icon</div>
        <!-- <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
        </nav> -->
      </div>
  </header>
</template>

<style>
header {
  position: fixed;
  top: 0;
  left: 0;
  margin: auto;
  width: 100%;
  background-color: var(--vt-c-black-soft);
  opacity: 0.6;
}

.navigation__header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 2.5rem;
}
</style>