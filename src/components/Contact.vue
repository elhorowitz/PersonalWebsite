<template>
  <div class="contact">
    <ul class="links">
      <li 
        v-for="link in links"
        v-bind:key="link.id"
      >
        <a 
          class="link" 
          target="_blank"
          v-bind:href="link.address" 
          @mouseover="focus"
          @mouseleave="unfocus"
          @focus="focus"
          @blur="unfocus"
        >
          <div class="icon">
            <GithubIcon v-if="link.id === 'github'" />
            <LinkedInIcon v-if="link.id === 'linkedin'" />
            <TwitterIcon v-if="link.id === 'twitter'" />
          </div>
          <span class="name">{{ link.name }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
import GithubIcon from './icons/github.vue';
import LinkedInIcon from './icons/linkedin.vue';
import TwitterIcon from './icons/twitter.vue';

export default {
  name: 'Contact',
  components: {
    GithubIcon,
    LinkedInIcon,
    TwitterIcon
  },
  data () {
    return {
      isActive: false,
      links: [
        {
          address: 'https://github.com/elhorowitz/',
          id: 'github',
          name: 'Github'
        },
        {
          address: 'https://www.linkedin.com/in/ericalhorowitz/',
          id: 'linkedin',
          name: 'LinkedIn'
        },
        {
          address: 'https://twitter.com/ElHorah',
          id: 'twitter',
          name: 'Twitter'
        },
      ]
    }
  },
  methods: {
    focus() {
      this.updateActive(true);
    },
    unfocus() {
      this.updateActive(false);
    }
  },
  props: {
    updateActive: Function
  }
}
</script>

<style scoped>
.contact {
  align-items: center;
  display: flex;
}
.links {
  display: flex;
  justify-content: space-between;
  list-style: none;
  margin: 2rem 0;
  margin-left: -1rem;
  padding: 0;
  width: 100%;
}
.link {
  align-items: center;
  color: var(--theme-white);
  display: flex;
  flex-direction: column;
  margin: 0 1rem;
  text-decoration: none;
}
.icon {
  border-radius: 50%;
  border: 0.25rem solid var(--theme-white);
  display: flex;
  padding: 1rem;
  position: relative;
  transition: border ease-in 0.2s;
}
.icon svg {
  height: 2rem;
  width: 2rem;
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
.link:focus {
  outline: none;
}
.link:focus .icon,
.link:hover .icon {
  border-color: var(--theme-white-transparent);
}
.link:focus .icon::after,
.link:hover .icon::after {
  border: 0.5rem solid var(--theme-white);
  bottom: -1rem;
  left: -1rem;
  right: -1rem;
  top: -1rem;
}
.link:focus .name,
.link:hover .name {
  font-weight: 500;
}
</style>
