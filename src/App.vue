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

* {
  box-sizing: border-box;
}

html,
body {
  font-size: 16px;
  height: 100%;
  margin: 0;
  padding: 0;
  width: 100%;
}

#app {
  font-family: var(--font-serif);
  height: 100%;
  min-width: 320px;
  min-height: 500px;
  overflow: hidden;
  width: 100%;
}
</style>
