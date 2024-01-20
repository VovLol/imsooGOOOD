<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Card 
  view=true
  foto="https://i.pinimg.com/originals/37/96/97/3796977afed95512ad5e7061a294323f.jpg"
  msg="hi!"/>
  <Card nft="top"
  view=true
  msg="Im the strongest, stop lookin at me lenya bistrov.... RYOKI TENKAI.... UNLIMITED VOID"
  foto="https://media.tenor.com/1GTTBuBsbq8AAAAM/gojo-purple-kyoshiki-murasaki.gif"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Card
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
