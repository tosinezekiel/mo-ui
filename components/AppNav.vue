<script setup lang="ts">
</script>
<template>
  <nav class="z-10 bg-gray-100 w-full fixed top-0">
    <div class="mx-auto max-w-8xl px-2 sm:px-12 lg:px-24">
      <div class="relative flex h-16 items-center justify-between">
        <div class="w-56">
          <h3 class="font-poppins text-xl text-gray-700">Shop</h3>
        </div>
        <div class="basis-2/4 flex justify-center">
          <img
            src="/images/modesigno-web.svg"
            alt="Modesigno"
            width="150"
            height="50"
          />
        </div>
        <div class="flex justify-between items-center pr-2 sm:pr-0 w-56">
          <NuxtLink to="/account/login"
            class="border border-black text-gray-700 rounded-sm px-4 py-2"
          >
            Login
          </NuxtLink>
          <MagnifyingGlassIcon
            class="ml-2 h-8 w-8 text-gray-700"
            aria-hidden="true"
          />
          <ShoppingCartIcon
            class="ml-2 h-8 w-8 text-gray-700 hover:-rotate-45 transition-transform duration-300 ease-in-out"
            aria-hidden="true"
          />
        </div>
      </div>
    </div>

    <div class="sm:hidden" id="mobile-menu">
      <div class="space-y-1 px-2 pb-3 pt-2"></div>
    </div>
  </nav>
</template>


<style scoped></style>
<script setup>
import { MagnifyingGlassIcon, ShoppingCartIcon } from '@heroicons/vue/24/solid'
</script>
