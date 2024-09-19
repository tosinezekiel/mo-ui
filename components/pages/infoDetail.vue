<template>
    <div class="mx-auto max-w-7xl lg:flex-auto">
      <div class="mx-auto mt-16 max-w-7xl sm:mt-20 lg:mt-24">
        <!-- <dl
          class="flex justify-between"
        >
          <div class="pl-8 flex justify-between">
            <dt class="text-base font-semibold leading-7 text-gray-900">
              <div
                class="flex h-10 w-10 justify-start"
              >
                <LightBulbIcon />
              </div>
            </dt>
            <dd class="ml-5 leading-7 text-gray-600 text-xs text-balance">
                <p class="font-semibold text-sm">
                    Endless Inspiration
                </p>
                200+ Designs: Explore a vast collection of unique 
                designs, available in various styles and colors.
            </dd>
          </div>
          <div class="pl-8 flex justify-between">
            <dt class="text-base font-semibold leading-7 text-gray-900">
              <div
                class="flex h-10 w-10 justify-start"
              >
              <ShieldExclamationIcon />
              </div>
            </dt>
            <dd class="ml-5 leading-7 text-gray-600 text-xs">
                <p class="font-semibold text-sm">
                    Unmatched Quality
                </p>
                Premium Materials: Feel the difference. Our merch 
                is crafted from quality materials built to last
            </dd>
          </div>
          <div class="pl-8 flex justify-between">
            <dt class="text-base font-semibold leading-7 text-gray-900">
              <div
                class="flex h-10 w-10 justify-start"
              >
              <GiftIcon />
              </div>
            </dt>
            <dd class="ml-5 leading-7 text-gray-600 text-xs">
                <p class="font-semibold text-sm">
                    Vote & Earn
                </p>
                Freebies: Your vote decides the next design! Be among 
                the first 10 voters on a winning design and score free merch
            </dd>
          </div>
        </dl> -->
        <section aria-labelledby="policies-heading" class="mt-12">
        <h2 id="policies-heading" class="sr-only">Our policies</h2>

        <div class="mx-auto max-w-7xl px-4 py-24 sm:px-6 sm:py-32 lg:px-8">
          <div class="grid grid-cols-1 gap-y-12 sm:grid-cols-2 sm:gap-x-6 lg:grid-cols-4 lg:gap-x-8 lg:gap-y-0">
            <div v-for="policy in policies" :key="policy.name" class="text-center md:flex md:items-start md:text-left lg:block lg:text-center">
              <div class="md:flex-shrink-0">
                <div class="flow-root">
                  <img class="-my-1 mx-auto h-24 w-auto" :src="policy.imageSrc" alt="" />
                </div>
              </div>
              <div class="mt-6 md:ml-4 md:mt-0 lg:ml-0 lg:mt-6">
                <h3 class="text-base font-medium text-gray-900">{{ policy.name }}</h3>
                <p class="mt-3 text-sm text-gray-500">{{ policy.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
      </div>
    </div>
</template>

<style scoped></style>
<script setup>
import {  LightBulbIcon } from "@heroicons/vue/24/outline";
import {  ShieldExclamationIcon } from "@heroicons/vue/24/outline";
import {  GiftIcon } from "@heroicons/vue/24/outline";
const policies = [
  {
    name: 'Free returns',
    imageSrc: 'https://tailwindui.com/img/ecommerce/icons/icon-returns-light.svg',
    description: 'Not what you expected? Place it back in the parcel and attach the pre-paid postage stamp.',
  },
  {
    name: 'Same day delivery',
    imageSrc: 'https://tailwindui.com/img/ecommerce/icons/icon-calendar-light.svg',
    description:
      'We offer a delivery service that has never been done before. Checkout today and receive your products within hours.',
  },
  {
    name: 'All year discount',
    imageSrc: 'https://tailwindui.com/img/ecommerce/icons/icon-gift-card-light.svg',
    description: 'Looking for a deal? You can use the code "ALLYEAR" at checkout and get money off all year round.',
  },
  {
    name: 'For the planet',
    imageSrc: 'https://tailwindui.com/img/ecommerce/icons/icon-planet-light.svg',
    description: 'We’ve pledged 1% of sales to the preservation and restoration of the natural environment.',
  },
];
</script>
