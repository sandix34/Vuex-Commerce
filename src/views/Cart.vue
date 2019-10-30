<template>
  <div>
    <h1 class="text-3xl">Cart</h1>
    <div class="w-5/6" v-if="cart">
      <div class="p-3" v-for="product in cart.products" :key="product.id">
        <i class="far fa-plus-square fa-lg pr-3 text-green-600"></i> 
        <i class="far fa-minus-square fa-lg pr-3 text-red-600"></i> 
        <span class="p-1 mr-2 shadow-lg text-2xl">{{ product.quantity }}</span>
        <span class="pr-3">{{ product.title }}</span>
        <span class="pr-3 shadow-lg text-2xl">{{ product.price }} €</span>
        <hr />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    cart() {
      return this.$store.getters.getCart;
    }
  }
};
</script>

<style lang="scss" scoped></style>
