<template>
  <div>
    <h1 class="text-3xl">Cart</h1>
    <div class="w-5/6" v-if="cart">
      <div class="p-2" v-for="product in cart.products" :key="product.id">
        <span class="pr-3 text-2xl">{{ product.quantity }}</span>
        <span class="pr-3">{{ product.title }}</span>
        <span class="pr-3 text-2xl">{{ product.price }} €</span>
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
