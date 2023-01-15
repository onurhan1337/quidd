<template>
  <div class="flex flex-col items-center my-12">
    <h1 class="text-md sm:text-xl font-bold">
      The page you are looking for was not found. 🧐
    </h1>
    <h3 class="text-md sm:text-xl font-semibold">To return to the homepage,</h3>
    <button @click="$router.back()" class="btn btn-primary my-6">
      &lt; Go Back
    </button>
  </div>
</template>
