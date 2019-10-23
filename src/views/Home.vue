<template>
  <div>
    <h1 class="text-5xl text-center pb-4 ">Book Shop</h1>
    <Products />
  </div>
</template>

<script>
import Products from "@/views/Products";

export default {
  name: "home",
  components: {
    Products
  }
};
</script>
