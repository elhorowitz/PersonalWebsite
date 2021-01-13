<template>
  <section class="landing">
    <div>
      <Heading />
      <Contact />
    </div>
    <img alt="cartoon" src="../assets/erica-cartoon.png" />
  </section>
</template>

<script>
import Contact from './Contact.vue'
import Heading from './Heading.vue'

export default {
  name: 'Landing',
  components: {
    Contact,
    Heading
  }
}
</script>

<style scoped>
.landing {
  align-items: center;
  background: var(--theme-green-dark);
  bottom: 0;
  display: flex;
  justify-content: center;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
}
</style>
