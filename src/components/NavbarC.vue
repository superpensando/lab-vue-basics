<template>
    <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </nav>
</template>

<script>
export default {
    name: 'NavbarC',
}
</script>

<style lang="scss">
nav {
    display: flex;
    justify-content: center;
    max-width: 600px;
    width: 100%;
    margin: 20px auto;
    padding: 20px 50px;
    background-color: green;
    color: white;

  a {
    font-weight: bold;
    color: #42b983;
    padding: 0 10px; 

    &.router-link-exact-active {
      color: white;
      text-decoration: none;
    }
  }
}
</style>