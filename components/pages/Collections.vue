<script setup>
  import { ChevronRightIcon } from '@heroicons/vue/24/outline'
</script>
<template>
    <div class="min-h-screen px-6 pt-10 sm:pt-12 pb-24 sm:pb-24 sm:px-24 lg:flex sm:justify-between lg:gap-x-10 lg:px-24 lg:py-10">
      <div class="mx-auto max-w-2xl lg:mx-0 lg:flex-auto">
        <h1 class="font-poppins mt-10 max-w-lg text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl">
          Choose from our creative collection
        </h1>
        <p class="mt-6 text-lg leading-8 text-gray-600">
          We have varieties of designs, we give you the best of the best.
        </p>
        <div class="mt-10 flex items-center gap-x-6">
          <button class="border border-black text-gray-700 rounded-full px-4 py-2 text-lg">
            Visit our collection
          </button>
          <a href="#" class="text-sm font-semibold leading-6 text-gray-900 flex items-center">
            <ChevronRightIcon />
          </a>
        </div>
      </div>
      <div class="grid grid-cols-2 gap-x-16 mt-10 lg:mt-0">
        <div class="relative pb-4 bg-gray-50 rounded-3xl shadow-lg w-44 h-48">
          <div class="bg-card-header absolute -top-1 flex justify-center items-center w-44 min-h-36 rounded-t-3xl px-6">
            <span class="w-56 inline-flex justify-center items-center rounded-full bg-blue-200 px-2 py-2 text-xs font-medium text-white ring-1 ring-inset ring-blue-700/10">
              Abstract
            </span>
          </div>
          <span class="w-full flex justify-center text-center text-gray-600 text-xs absolute bottom-6">104+ Designs</span>
        </div>
        <div class="relative pb-4 bg-gray-50 rounded-3xl shadow-lg w-44 h-48">
          <div class="bg-card-header absolute -top-1 flex justify-center items-center w-44 min-h-36 rounded-t-3xl px-6">
            <span class="w-56 inline-flex justify-center items-center rounded-full bg-red-200 px-2 py-2 text-xs font-medium text-white">
              Social Media
            </span>
          </div>
          <span class="w-full flex justify-center text-center text-gray-600 text-xs absolute bottom-6">390+ Designs</span>
        </div>
        <div class="relative pb-4 bg-gray-50 rounded-3xl shadow-lg w-44 h-48">
          <div class="bg-card-header absolute -top-1 flex justify-center items-center w-44 min-h-36 rounded-t-3xl px-6">
            <span class="w-56 py-2 inline-flex items-center rounded-full bg-green-200 justify-center text-xs font-medium text-white">
              Software
            </span>
          </div>
          <span class="w-full flex justify-center text-center text-gray-600 text-xs absolute bottom-6">111+ Designs</span>
        </div>
        <div class="relative pb-4 bg-gray-50 rounded-3xl shadow-lg w-44 h-48">
          <div class="bg-card-header absolute -top-1 flex justify-center items-center w-44 min-h-36 rounded-t-3xl px-6">
            <span class="w-56 inline-flex justify-center items-center rounded-full bg-gray-200 px-2 py-2 text-xs font-medium text-white">
              Programming
            </span>
          </div>
          <span class="w-full flex justify-center text-center text-gray-600 text-xs absolute bottom-6">70+ Designs</span>
        </div>
      </div>
    </div>
  </template>
  
  
  <style scoped>
  
  </style>
  