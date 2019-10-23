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
        <router-link to="/cart">Cart (0)</router-link>
      </span>
    </div>
    <router-view />
  </div>
</template>

<style>
#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
