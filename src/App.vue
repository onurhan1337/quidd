<script setup>
import { RouterView } from 'vue-router'
import Navbar from '@/components/navbar/NavBar.vue'
</script>

<template>
  <header class="container flex mx-auto flex-col items-center my-8">
    <div class="avatar">
      <div class="w-36 rounded-full">
        <img alt="Quidd logo" src="@/assets/logo.jpg" />
      </div>
    </div>

    <div class="wrapper my-2">
      <Navbar />
    </div>
  </header>

  <RouterView />
</template>
