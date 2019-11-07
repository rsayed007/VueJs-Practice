<template>
  <div id="app">
    <Navbar @search="search"></Navbar>
    <div class="container">
      <div class="row">
        <div class="col-sm-9">
          <Inventory @newItemAdded="addCartItems" :items="items" ></Inventory>
        </div>
        <div class="col-sm-3">
          <Cart @itemRemove="removeCartItem" :items="cart"></Cart>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import Navbar from './components/Nav'
import Cart from './components/Cart'
import Inventory from './components/Inventory'
import Data from './data/data.js'

export default {
  components: {
    Navbar,
    Cart,
    Inventory
  },
  data () {
    return {
      items: [],
      cart: []
    }
  },
  mounted () {
    this.items = Data
  },
  methods: {
    search (keyword) {
      this.items = Data.filter(item => {
        return item.title.toLowerCase().indexOf(keyword.toLowerCase()) !== -1
      })
    },
    addCartItems (item) {
      this.cart.push(item)
    },
    removeCartItem(index){
      this.cart.splice(index,1)
    }
  },
  
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
.container{
    padding-top: 20px;
  }
</style>
