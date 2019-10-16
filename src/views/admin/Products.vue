<template>
  <div>
    <router-link to="/admin/product-add" class="no-underline hover:underline text-blue-500 text-lg font-extrabold p-8">Add new book</router-link>
    <ProductList />
  </div>
</template>

<script>
import ProductList from '@/components/admin/ProductList';

export default {
	components: {
		ProductList,
	}, 
};
</script>
