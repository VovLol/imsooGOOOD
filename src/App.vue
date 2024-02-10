<template>
  <div class="container">
    <h1>Emit test</h1>
  </div>
  <HelloWorld />
  <div class="rows">
    <button v-on:click="addAnimal" type="button" class="btn btn-primary">Butt</button>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  provide:{
    animal: "slon"
  },
  methods:{
    addAnimal(){
      this.animal = this.animal + " " + this.animal
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
