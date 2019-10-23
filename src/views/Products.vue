<template>
  <div class="flex flex-wrap" v-if="products">
    <div
      class="relative flex-col justify-between p-2 m-2 w-64 shadow"
      v-for="product in products"
      :key="product.id"
    >
      <div class="p-4">{{ product.title }}</div>
      <div class="flex justify-center p-2">
        <img
          class="w-auto inline-block shadow-2xl mb-12"
          alt="book image"
          :src="product.image"
        />
      </div>
      <div class="absolute inset-x-0 bottom-0 flex flex-row justify-around">
        <div class="text-3xl">
          {{ product.price }}<span class="text-base font-semibold"> €</span>
        </div>
        <button
          @click="addToCart(product)"
          class="text-blue-500 font-extrabold underline"
        >
          Add to cart
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  created() {
    this.$store.dispatch("getProducts");
  },
  computed: {
    products() {
      return this.$store.state.products;
    }
  },
  methods: {
    addToCart(product) {
      this.$store.dispatch("addToCart", product).then(() => {
        console.log(this.$store.state.cart);
      });
    }
  }
};
</script>
