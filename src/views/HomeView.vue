<template>
  <div class="home">
    <div>
      <h3>Iteration 2 | Display the result of a Javascript operation in a component's HTML</h3>
      <input type="number" v-model="num1" />
      <input type="number" v-model="num2" />
      <p> {{result}}</p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'HomeView',
  data() {
    return {
      num1:0,
      num2:1,
    }
  },
  computed: {
    result() {
      return this.num1 + this.num2;
    }
  }

}
</script>
