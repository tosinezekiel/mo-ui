<script setup lang="ts">
</script>
<template>
  <div
    class="bg-image flex flex-col min-h-screen bg-cover bg-center justify-center"
  >
    <AppNav />
    <div class="flex flex-col items-start w-2/3 p-24 space-y-4">
      <h1
        class="font-poppins mt-10 max-w-lg text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl"
      >
        Wear it like you mean it.
      </h1>
      <p class="font-poppins font-light text-small text-gray-700">
        Everything made of quality materials for creative enthusiast <br />
        supporting technology at large.
      </p>
      <button
        class="w-48 border-gray-700 border-2 rounded-none px-4 py-2 text-lg"
      >
        Shop now
      </button>
      <ul class="flex justify-between ml-2 text-gray-800 w-96">
        <li class="list-disc">Free sign up</li>
        <li class="list-disc">No charges</li>
        <li class="list-disc">Over 100+ Designs</li>
      </ul>
    </div>
    <div
      class="capitalize absolute bottom-6 text-gray-700 flex justify-between items-start w-1/3 px-24"
    >
      <span>Men</span>
      <span>Women</span>
      <span>Kids</span>
    </div>
  </div>
</template>

<style scoped>
.bg-image {
  background: url("/images/bg.png");
}
</style>
