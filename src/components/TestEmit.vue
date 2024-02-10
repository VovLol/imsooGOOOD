<template>
    <div class="rows">
        <div class="input-group mb-3">
            <input type="text"  v-model="userName" class="form-control" placeholder="Username" aria-label="Username">
        </div>
      <button v-on:click="sendNigger" type="button" class="btn btn-danger">Make it HURT</button>

      <div class="rows">
        Animals: {{ animal }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'TestEmit',
    emits:['msg'],

    data(){
        return{
            userName: ''
        }
    },

    methods:{
        sendNigger(){
          this.$emit('msg', this.userName);
        }
    },
    inject:['animal']
  }
  </script>
  
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  </style>
  