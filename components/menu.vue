<template>
  <div class="menu-menu" v-bind:class="rootClassName">
    <nuxt-link to="/" class="menu-navlink">{{ text }}</nuxt-link>
    <div class="menu-container">
      <nuxt-link to="/resume" class="menu-navlink1">{{ text2 }}</nuxt-link>
      <nuxt-link to="/projects" class="menu-navlink2">{{ text3 }}</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  props: {
    rootClassName: String,
    text: {
      type: String,
      default: 'Jason Guthrie',
    },
    link_text: {
      type: String,
      default: 'https://example.com',
    },
    text3: {
      type: String,
      default: 'Projects',
    },
    text2: {
      type: String,
      default: 'Resume',
    },
  },
}
</script>

<style scoped>
.menu-menu {
  flex: 0 0 auto;
  width: 100%;
  height: 100px;
  display: flex;
  box-shadow: 5px 5px 10px 0px rgba(0, 0, 0, 0.21);
  align-items: flex-start;
  padding-top: 0px;
  padding-left: var(--dl-space-space-threeunits);
  padding-right: var(--dl-space-space-threeunits);
  justify-content: space-between;
  background-image: linear-gradient(225deg, rgb(0, 255, 193) 2.00%,rgb(0, 191, 204) 100.00%);
}
.menu-navlink {
  font-size: 24px;
  align-self: center;
  font-style: normal;
  font-family: Noto Sans;
  font-weight: 700;
  text-decoration: none;
}
.menu-container {
  display: flex;
  align-self: center;
  align-items: flex-start;
  justify-content: flex-start;
}
.menu-navlink1 {
  padding-left: var(--dl-space-space-unit);
  text-decoration: none;
}
.menu-navlink2 {
  padding-left: var(--dl-space-space-unit);
  text-decoration: none;
}


</style>
