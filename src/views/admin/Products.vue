<template>
  <div>
    <div class="text-right">
      <router-link
        to="/admin/product-add"
        class="m-8 px-3 py-3 font-medium bg-blue-500 rounded-lg text-white hover:bg-blue-300 focus:outline-none focus:bg-blue-300"
        >Add new book</router-link
      >
    </div>
    <ProductList />
  </div>
</template>

<script>
import ProductList from "@/components/admin/ProductList";

export default {
  components: {
    ProductList
  }
};
</script>
