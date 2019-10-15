<template>
  <div class="flex justify-center">
    <table class="table-auto">
      <thead class="bg-gray-200 uppercase text-grey-400">
        <tr class="border-t border-gray-300 text-gray-600">
          <th class="px-10 py-2 ">id</th>
          <th class="px-10 py-2">Title</th>
          <th class="px-10 py-2">Author</th>
          <th class="px-10 py-2">Publisher</th>
          <th class="px-10 py-2">Year</th>
          <th class="px-10 py-2">Image</th>
          <th class="px-10 py-2"></th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="product in products" :key="product.id" class="hover:bg-blue-100 border-t border-gray-300">
          <th class="p-4">{{ product.id }}</th>
          <td class="p-4">{{ product.title }}</td>
          <td class="p-4">{{ product.author.firstName }} {{ product.author.name }}</td>
          <td class="p-4">{{ product.publisher }}</td>
          <td class="p-4">2{{ product.year }}</td>
          <td class="p-4">im{{ product.image }}</td>
          <td class="p-4 text-blue-500">
            <button class="px-2 hover:bg-white">Edit</button>
            <span>|</span>
            <button class="px-2 hover:bg-white">Delete</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import productService from '../../services/productService';

export default {
  data() {
    return {
      products: [],
    }
  },
  created() {
    productService.getProducts().then(res => {
      console.log(res);
      this.products = res.data;
      
    })
  }
};
</script>
