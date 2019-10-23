<template>
  <div class="flex flex-col">
    <h3 class="text-center text-2xl text-gray-600 font-bold tracking-wide">
      Create a new book
    </h3>
    <ProductForm />
  </div>
</template>

<script>
import ProductForm from "@/components/admin/ProductForm";

export default {
  components: {
    ProductForm
  }
};
</script>
