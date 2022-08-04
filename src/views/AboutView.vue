<template>
  <div class="about">
    <h1>Exercices Lessons</h1>
    <article>
      <button v-if="!signedIn">V-if Log In</button>
      <button v-if="signedIn">V-if Log Out</button>
    </article>
      <article>
      <button v-if="!signedIn">V-if Log In</button>
      <button v-else>V-else Log Out</button>
    </article>
     <article>
    <button v-show="!signedIn">V-show Log In</button>
    <button v-show="signedIn">V-show Log Out</button>
  </article>
  </div>
</template>
<script>
export default {
  data() {
    return {
      signedIn:true
    }
  }
}
</script>