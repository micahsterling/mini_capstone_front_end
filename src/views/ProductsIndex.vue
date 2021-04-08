<template>
  <div class="products-index">
    <h1>{{ message }}</h1>
   <div class="row">
      <div class="col-sm-4" v-for="product in products">
        <div class="card">
           <img style="width: 200px" v-bind:src="product.image_url" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">{{product.name}}</h5>
            <p class="card-text">{{product.description}}</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
          </div>
        </div>
        <br />
        <br />
      </div>
    </div>
  </div>
</template>

<style>
</style>

<script>
import axios from "axios";
export default {
  data: function () {
    return {
      message: "Welcome to index!",
      products: [],
    };
  },
  created: function () {
    this.productsIndex();
  },
  methods: {
    productsIndex: function () {
      console.log("index page");
      // make a web request to backend
      axios.get("api/products").then((response) => {
        console.log(response.data);
        this.products = response.data;
      });
    },
  },
};
</script>

