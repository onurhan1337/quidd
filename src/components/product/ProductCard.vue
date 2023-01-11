<template>
  <li v-for="prod in products" :key="prod.id">
    {{ prod.name }}
  </li>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          id: 1,
          name: 'Macbook air',
          price: 20000,
          categoryName: 'technology'
        },
        {
          id: 2,
          name: 'Basic Black Tshirt',
          price: 25,
          categoryName: 'clothes'
        },
        {
          id: 3,
          name: 'Lenovo ideapad',
          price: 7000,
          categoryName: 'technology'
        },
        {
          id: 4,
          name: 'Apple',
          price: 2,
          categoryName: 'food'
        }
      ]
    }
  }
}
</script>
