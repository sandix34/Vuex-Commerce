<template>
  <div>
    <div class="text-center">
      <router-link
        to="/admin/product-add"
        class="m-8 px-3 py-3 font-medium bg-blue-500 rounded-lg text-white hover:bg-gray-400 focus:outline-none focus:bg-gray-400"
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
