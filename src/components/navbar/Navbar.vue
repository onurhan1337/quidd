<template>
  <nav class="navbar rounded-full">
    <ul class="menu menu-horizontal px-8 py-4 shadow shadow-pink-500 bg-base-100 rounded-box space-x-8">
      <NavbarItem />
    </ul>
  </nav>
</template>

<script>
import NavbarItem from '@/components/navbar/NavbarItem.vue'
import { defineComponent } from 'vue'

export default defineComponent({
  components: { NavbarItem }
})
</script>
