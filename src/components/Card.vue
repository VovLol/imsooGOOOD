<template>
 <div class="card">
  <div class="card" style="width: 18rem;">
    <img v-if="openImg" v-bind:src="foto" class="card-img-top" alt="...">
   <div class="card-body">
    <p class="card-text">{{msg}}</p>
    <p class="card-text">{{msg}}</p>
   </div>
   <button v-on:click="remove" type="button" class="btn btn-primary">{{msgBtn}}</button>
  </div>
 </div> 
</template>

<script>
/* eslint-disable */
export default {
  name: 'Card',
  props: {
    msg: String,
    nft: String,
    foto: String,
    view: Boolean
  },
  data(){
    return{
     openImg: true,
     msgBtn: "200%"
    }
  },
  methods:{
    remove(){
      this.openImg = !this.openImg;
      if(this.openImg){
        this.msgBtn = "200% HOLLLLLOW PURPL"
      }else{
        this.msgBtn = "unhollow purple"
      }
    }
  }
}
</script>

<style scoped>

</style>
