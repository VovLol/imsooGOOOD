<template>
  <div class="rows">
    <div class="alert alert-danger" role="alert">
      Message : {{ textMsg }}
    </div>
    <TestEmit v-on:msg="showMsg" v-model="top" />
  </div>
</template>

<script>
import TestEmit from '@/components/TestEmit.vue'
export default {
  name: 'HelloWorld',
  components:{
    TestEmit
  },

  data(){
    return{
     textMsg:'',
    }
  },
  
  methods:{
    showMsg(e){
     this.textMsg = "This sigma nicknam is" + `${e}`
    }
  }
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
