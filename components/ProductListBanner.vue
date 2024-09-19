<script>
import { PlayCircleIcon, MagnifyingGlassIcon } from "@heroicons/vue/24/solid";
</script>
<template>
  <div
    class="flex flex-col bg-gray-50 justify-center max-h-96 relative"
  >
    <AppNav />
    <div class="flex flex-col items-center text-center w-full p-24 space-y-4">
      <p
        class="font-poppins mt-10 max-w-lg text-2xl font-light tracking-tight text-gray-900 sm:text-sm"
      >
      Best ways to get comfy in  style
      </p>
      <p class="font-poppins font-semibold text-3xl text-gray-500">
        Place a vote, Get a chance to win amazing <br> points
      </p>
      <NuxtLink
        class="w-48 border-yellow-300 flex border-2 rounded-full py-2 px-2 text-lg"
      >
        <PlayCircleIcon class="text-yellow-500 h-8 w-8 mr-5" />
        <span class="font-light text-base">Let me vote</span>
      </NuxtLink>
    </div>
    <div class="w-full flex justify-center">
    <div class="relative w-2/3">
      <MagnifyingGlassIcon 
      class="absolute left-16 top-1/2 transform -translate-y-1/2 h-5 w-5 text-gray-400"
      />
      <input type="text" class="w-full h-32 px-24 py-10 border rounded-full" placeholder="Search a product..." />
    </div>
  </div>

  </div>
</template>

<style scoped>

</style>
