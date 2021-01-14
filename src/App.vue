<template>
  <Landing />
</template>

<script>
import Landing from './components/Landing.vue'

export default {
  name: 'App',
  components: {
    Landing
  }
}
</script>

<style>
:root {
  --font-sans: 'Raleway', sans-serif;
  --font-serif: 'Josefin Slab', serif;

  --theme-green-dark: #47584D;
  --theme-white: #FAF5D3;
  --theme-white-transparent: rgba(250, 245, 211, 0.4);
}

html {
  font-size: 16px;
}

#app {
  font-family: var(--font-serif);
}
</style>
