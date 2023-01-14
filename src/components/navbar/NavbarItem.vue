<template>
  <RouterLink
    v-for="link in links"
    to="{{link.slug}}"
    class="navbar-item"
    :key="link.name"
  >
    {{ link.name }}
  </RouterLink>
</template>

<script>
export default {
  data() {
    return {
      // TODO: currently not working, will update via vue-router. see https://router.vuejs.org/guide/#javascript
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
  },
}
</script>
