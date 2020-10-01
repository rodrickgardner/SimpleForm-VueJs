<template>
  <div id="add-form">
    <h2>Add a New Item</h2>
    <form>
    <label>Name</label>
    <input type="text" v-model.lazy="name" required placeholder="Name">

    <label>Quantity</label>
    <!--<input type="text"v-model.lazy="quantity" required>-->
    <input :value="quantity" @change="updateQuantity" type="number" class="form-control" name="quantity" id="quantity" placeholder="Quantity">



    <label>Unit Price</label>
    <!--<input type="text"v-model.lazy="price" required>-->
    <input :value="price"  @change="updateRate" type="number" step="any" class="form-control" name="price" id="price" placeholder="Price">

    <label>Total</label>
    <!--<input type="text"v-model.lazy="total" required>-->

    <input v-model="total" type="number" step="any" class="form-control" name="total" id="total" placeholder="Total Price">

    </form>

    <div id="preview">
      <h3>Preview</h3>
      <p>Name:{{name}}</p>
      <p>Quantity:{{quantity}}</p>
      <p>Unit Price:{{price}}</p>
      <p>Total:{{total}}</p>
    </div>
    <button>Save</button>
    <button type="reset">Clear</button>
  </div>
</template>

<script>
export default {
  

  data(){
    return{
    name:"",
    quantity:"",
    price:"",
    total:""


    }
  },
  methods:{

    updateQuantity(event) {
        this.quantity = event.target.value
        this.total = this.quantity * this.price
    },
    updateRate(event) {
        this.price = event.target.value
        this.total = this.quantity * this.price
    }


  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
 