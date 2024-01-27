<template>
<div class="rows">

  <form class="row g-3">
    <div class="col-auto">
     <label for="inputName" class="visually-hidden">Название</label>
     <input v-model="part" type="text" class="form-control" id="staticEmail2" placeholder="Вводи">
    </div>
    <div class="col-auto">
      <label for="inputPrace" class="visually-hidden">Цена</label>
      <input v-model="price" type="text" class="form-control" id="inputPassword2" placeholder="топ">
    </div>
    <div class="col-auto">
      <label for="inputToValue" class="visually-hidden">Кол-во</label>
      <input v-model="volume" type="text" class="form-control" id="inputPassword2" placeholder="вводи">
    </div>
    <div class="col-auto">
     <button type="submit" v-on:click="added" class="btn btn-primary mb-3">Confirm</button>
    </div>
  </form>
  <button v-on:click="show" class="btn btn-primary mb-3">посмот</button>

  <div v-if="true" class="row">
    <ul id="array-rendering">
      <li v-for="item in product" :key="item.PName" >
       {{ item.PName }} <br/>
       {{ item.Price }} <br/>
       {{ item.PVolume }} <br/>
      </li>
    </ul>

  </div>

  <div v-if="true" class="row">
    <ul id="array-rendering">
      <li v-for="item in test" :key="item.PName" >
      </li>
    </ul>

  </div>

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
      product: [
      {
        PName:"aaa",
        Price:10,
        PVolume:42
      }
    ],
      product: [],
      part: "",
      volume: 0,
      price: 0,
      check: false,
      test: [1, 2, 3, 4]
     }
  },
  methods:{
    added(){
      let p = new Product(this.part, this.price, this.volume);
      this.product.push(p)
      console.table(this.product[0])
    },
    show(){
    this.check = !this.check
    alert(this.check)
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
