<template>
  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
  </nav>

  <RouterView />
</template>

<style>
@import '@/assets/base.css';

#app {
  display: flex;
  flex-direction: column;
  margin: 0 auto;
  padding: 2em;
  font-weight: normal;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2em;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

nav {
  display: flex;
  justify-content: center;
  font-size: 0.75em;
  margin-top: 2em;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: flex;
  padding: 0 1em;
  border-left: 0.0625em solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
</style>