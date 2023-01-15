<template>
  <router-link to="/" class="navbar-item">
    Home
  </router-link>
  <router-link to="/cart" class="navbar-item">
    Cart
  </router-link>
  <router-link to="/checkout" class="navbar-item">
    Checkout
  </router-link>
</template>

<script>
import HomeView from '@/views/HomeView.vue'
import NotFound from '@/views/NotFound.vue'

export default {
  data() {
    return {
     components: {
        HomeView,
        NotFound
      }
    }
  },
}
</script>
