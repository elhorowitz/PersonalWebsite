<template>
  <ul class="contact">
    <li 
      v-for="link in links"
      v-bind:key="link.id"
    >
      <a class="link" v-bind:href="link.address" target="_blank">
        <div class="icon"></div>
        <span class="name">{{ link.name }}</span>
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Contact',
  data () {
    return {
      links: [
        {
          address: 'https://github.com/elhorowitz/',
          id: 'github',
          name: 'Github',
        },
        {
          address: 'https://www.linkedin.com/in/ericalhorowitz/',
          id: 'linkedin',
          name: 'LinkedIn',
        },
        {
          address: '',
          id: 'resume',
          name: 'Resume',
        },
        {
          address: 'https://twitter.com/ElHorah',
          id: 'twitter',
          name: 'Twitter',
        },
      ]
    }
  } 
}
</script>

<style scoped>
.contact {
  display: flex;
  justify-content: space-between;
  list-style: none;
  margin: 2rem 0;
  padding: 0;
}
.link {
  align-items: center;
  color: var(--theme-white);
  display: flex;
  flex-direction: column;
  margin: 0;
  text-decoration: none;
}
.icon {
  border-radius: 50%;
  border: 0.25rem solid var(--theme-white);
  height: 4rem;
  position: relative;
  transition: border ease-in 0.2s;
  width: 4rem;
}
.icon::after {
  border-radius: 50%;
  border: 0 solid transparent;
  bottom: 0;
  content: '';
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  transition: all ease-in 0.2s;
}
.name {
  font-family: var(--font-sans);
  font-weight: 300;
  margin-top: 1rem;
  transition: all ease-in 0.2s;
}

.link:hover .icon {
  border-color: var(--theme-white-transparent);
}
.link:hover .icon::after {
  border: 0.5rem solid var(--theme-white);
  bottom: -1rem;
  left: -1rem;
  right: -1rem;
  top: -1rem;
}
.link:hover .name {
  font-weight: 500;
}
</style>
