<template>
  <section class="landing">
    <div>
      <Heading />
      <Contact :updateActive="setActive" />
    </div>
    <Cartoon :isActive="isActive" />
  </section>
</template>

<script>
import Cartoon from './Cartoon';
import Contact from './Contact';
import Heading from './Heading';

export default {
  name: 'Landing',
  components: {
    Cartoon,
    Contact,
    Heading
  },
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    setActive(bool) {
      this.isActive = bool;
      console.log('isActive set to: ', this.isActive)
    }
  }
}
</script>

<style scoped>
.landing {
  align-items: center;
  background: var(--theme-green-dark);
  border: 1rem solid var(--theme-white-transparent);
  bottom: 0;
  display: flex;
  justify-content: center;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
}
.landing::before {
  border: 0.25rem solid var(--theme-white);
  bottom: 0.5rem;
  content: '';
  left: 0.5rem;
  position: absolute;
  right: 0.5rem;
  top: 0.5rem;
}
</style>
