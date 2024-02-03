<template>
<div class="rows">
<slot>  </slot>

  <div class="row g-3">
    <div class="col-auto">
     <label for="inputName" class="visually-hidden">Название</label>
     <input v-model="part.PName" type="text" class="form-control" id="staticEmail2" placeholder="Вводи">
    </div>
    <div class="col-auto">
      <label for="inputPrace" class="visually-hidden">Цена</label>
      <input v-model="part.Price" type="text" class="form-control" id="inputPassword2" placeholder="топ">
    </div>
    <div class="col-auto">
      <label for="inputToValue" class="visually-hidden">Кол-во</label>
      <input v-model="part.PVolume" type="text" class="form-control" id="inputPassword2" placeholder="вводи">
    </div>
    <div class="col-auto">
     <button type="submit" v-on:click="added" class="btn btn-primary mb-3">Confirm</button>
    </div>
  </div>

  <button v-on:click="show" class="btn btn-primary mb-3">посмот</button>
  <slot> </slot>

  <div v-if="check" class="row">
    <ul id="array-rendering">
      <li v-for="item in product" :key="item.PName" >
       {{ item.PName }}   {{ item.Price }}  {{ item.PVolume }} <br/>
      </li>
    </ul>

  </div>

  <div class="alert alert-primary" role="alert">
  THIS product is over than 30 KG i think: {{resultSumm}}
</div>


  <!-- <div v-if="true" class="row">
    <ul id="array-rendering">
      <li v-for="item in test" :key="item.PName" >
      </li>
    </ul>

  </div> -->

</div>
</template>

<script>
/* eslint-disable */
import Product from '../Product.js'
export default {
  name: 'card',
  props: {
    msg: String
  },
  data(){
     return{
      product: [],
      part: Product,
      check: false,
     };
  },
  methods:{
    added(){
      this.product.push({...this.part})
    },
    show(){
    this.check = !this.check
  },
 },
 computed : {
   resultSumm(){
    return this.product.length
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
