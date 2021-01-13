<template>
  <header class="heading">
    <h1 class="title">Erica Horowitz</h1>
    <h2 class="description">Frontend Engineer</h2>
  </header>
</template>

<script>
export default {
  name: 'Heading'
}
</script>

<style scoped>
.heading {
  background: var(--theme-green-dark);
  color: var(--theme-white);
  font-family: var(--font-sans);
}
.title {
  font-size: 2.625rem;
  font-weight: 700;
  line-height: 1;
  margin: 0;
  text-transform: uppercase;
}
.description {
  font-size: 1.5rem;
  font-weight: 300;
  line-height: 1.5;
  margin: 0;
}
</style>
