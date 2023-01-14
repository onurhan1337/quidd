<template>
  <li
    class="my-5 xl:w-1/4 md:w-1/2 p-4"
    v-for="prod in products"
    :key="prod.id"
  >
    <div class="card h-full bg-base-100 shadow-md">
      <figure class="h-full">
        <img class="h-full" :src="prod.imageUrl" alt="Shoes" />
      </figure>
      <div class="card-body">
        <div class="flex flex-row justify-between">
          <div class="badge badge-outline">{{ prod.categoryName }}</div>
          <!-- if product have discount, the price will be calculated dynamically according to the discount rate -->
          <h2 v-if="prod.hasDiscount" class="font-bold">
            {{ calcDiscountedPrice(prod.price, prod.discountRate) }}₺
          </h2>
          <h2 v-else class="font-bold">{{ prod.price }}₺</h2>
        </div>
        <h2 class="card-title">
          {{ prod.name }}
          <!-- if production has discount, badge will be visible -->
          <div
            v-if="prod.hasDiscount"
            class="badge badge-secondary justify-end"
          >
            -{{ prod.discountRate }}%
          </div>
        </h2>
        <!-- I'm really lazy so lorem ipsum... but if you use it add description prop to product -->
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. In elit
          neque, mattis a neque rhoncus.
        </p>
        <div class="card-actions">
          <button class="btn btn-outline btn-secondary">Sepete Ekle</button>
        </div>
      </div>
    </div>
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
          imageUrl:
            'https://store.storeimages.cdn-apple.com/4668/as-images.apple.com/is/macbook-air-midnight-select-20220606?wid=904&hei=840&fmt=jpeg&qlt=90&.v=1653084303665',
          price: 20000,
          hasDiscount: true,
          discountRate: 10,
          categoryName: 'technology'
        },
        {
          id: 2,
          name: 'Basic Black Tshirt',
          imageUrl:
            'https://cdn.cimri.io/image/320x320/asus-vivobook-15-x1502za-ej773-intel-core-i5-1240p-8-gb-ram-512-gb-ssd-freedos-156-fhd-tasinabilir-bilgisayar_661543961.jpg',
          price: 25,
          hasDiscount: false,
          categoryName: 'clothes'
        },
        {
          id: 3,
          name: 'Lenovo ideapad',
          imageUrl:
            'https://cdn.vatanbilgisayar.com/Upload/PRODUCT/lenovo/thumb/135948-2_large.jpg',
          price: 7000,
          hasDiscount: true,
          discountRate: 15,
          categoryName: 'technology'
        },
        {
          id: 4,
          name: 'Apple',
          imageUrl:
            'https://images.pexels.com/photos/102104/pexels-photo-102104.jpeg?auto=compress&cs=tinysrgb&w=300',
          price: 2,
          hasDiscount: false,
          categoryName: 'food'
        }
      ]
    }
  },
  methods: {
    calcDiscountedPrice(price, discountRate) {
      return (price * (100 - discountRate)) / 100
    }
  }
}
</script>
