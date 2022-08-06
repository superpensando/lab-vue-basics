<!-- eslint-disable vue/no-unused-vars -->
<!-- eslint-disable vue/valid-v-for -->
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
    <div>
      <h3>Iteration 4 | Display a list of elements that are stored inside a component</h3>
      <div class="posts">
        <PostC  v-for="post in posts" :title="post.title" :description="post.description" :content="post.content" :idPost="post.id" :key="post.id"/>
      </div>
    </div>
    <div>
      <h3>Iteration 5 | Bonus | Change the background color of an element when pressing a button</h3>
      <div>
        <div :class="changeColor ? 'isChangeColor' : ''">Cambio de color</div>
        <button @click="changeColor = !changeColor">Click for change Color</button>
      </div>
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
import PostC from '@/components/PostC.vue'
export default {
  name: 'HomeView',
  components: {
    PostC
  },
  data() {
    return {
      num1:0,
      num2:1,
      signedIn:false,
      changeColor:false,
      posts: [
        {
          id: 1,
          title:"Título",
          description:"Description",
          content: "Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum"
        },
         {
          id: 2,
          title:"Título",
          description:"Description",
          content: "Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum"
        },
         {
          id: 3,
          title:"Título",
          description:"Description",
          content: "Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum"
        },
         {
          id: 4,
          title:"Título",
          description:"Description",
          content: "Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum"
        },
      ]
    }
  },
  computed: {
    result() {
      return this.num1 + this.num2;
    }
  },

}
</script>


<style lang="scss">
.posts {
   display:flex; 
   margin: 0 auto;
   max-width:600px;
   width:100%;
}
.isChangeColor {
  max-width:600px;
  width:100%;
  background-color: green;
  color:white;
  margin:0 auto; 
}
</style>
