<template>
  <NavbarC />
  <router-view/>
  <FooterC />
</template>

<script>
import FooterC from '@/components/FooterC.vue'
import NavbarC from '@/components/NavbarC.vue'


export default {
  components: {
    FooterC,
    NavbarC,
}
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
