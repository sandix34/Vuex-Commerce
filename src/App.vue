<template>
  <div id="app" class="p-4">
    <div id="nav" class="font-semibold p-8 text-gray-700">
      <span class="p-2 relative">
        <router-link to="/">Home</router-link>
      </span>
      <span class="p-2">
        <router-link to="/contact">Contact</router-link>
      </span>
      <span class="p-2">
        <router-link to="/admin">Admin</router-link>
      </span>
      <span class="p-8 absolute top-0 right-0">
        <router-link to="/cart"
          ><i class="fas fa-shopping-cart p-2"></i>Cart ({{
            numberArticlesInCart
          }})</router-link
        >
      </span>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  computed: {
    numberArticlesInCart() {
      return this.$store.getters.getNumberArticleInCart;
    }
  }
};
</script>

<style>
#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
