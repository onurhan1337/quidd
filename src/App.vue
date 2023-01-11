<script setup>
import { RouterView } from 'vue-router'
import Navbar from '@/components/navbar/Navbar.vue'
</script>

<template>
  <header class="container flex mx-auto flex-col items-center my-8">
    <div class="avatar">
      <div class="w-36 rounded-full">
        <img
          alt="Quidd logo"
          src="@/assets/logo.jpg"
        />
      </div>
    </div>

    <div class="wrapper my-6">
      <Navbar />
    </div>
  </header>

  <RouterView />
</template>
