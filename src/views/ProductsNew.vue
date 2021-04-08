<template>
  <div class="product-new">
    <h1>{{ message }}</h1>
    <div>
      <p> Name: <input type="text"></p>
      <p> Description: <input type="text"></p>
      <p> image_url: <input type="text"></p>
      <p> Price: <input type="text"></p>
    </div>
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function () {
    return {
      message: "Add a product",
    };
  },
  created: function () {},
  methods: {},
};
</script>