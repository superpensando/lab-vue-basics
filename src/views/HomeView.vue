<template>
  <div class="home">
    <div>
      <h3>Iteration 2 | Display the result of a Javascript operation in a component's HTML</h3>
      <input type="number" v-model="num1" />
      <input type="number" v-model="num2" />
      <p> {{result}}</p>
    </div>
    <div>
 
      <h3>Iteration 3 | Show an element only if a particular property is set to true</h3>
      <button @click="signedIn = !signedIn">Click and Show</button>
      <br/>
      <button  v-show="!signedIn">Is signedIn is FALSE, show this</button>
      <button  v-show="signedIn">Is signedIn is TRUE, show this</button>
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
      signedIn:false
    }
  },
  computed: {
    result() {
      return this.num1 + this.num2;
    }
  }

}
</script>
