<template>
  <RouterLink v-for="link in links" to="{{link.slug}}" class="navbar-item" :key="link.name">
    {{ link.name }}
  </RouterLink>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          slug: '/',
          name: 'Home'
        },
        {
          slug: '/cart',
          name: 'Cart'
        },
        {
          slug: '/checkout',
          name: 'Checkout'
        }
      ]
    }
  }
}
</script>