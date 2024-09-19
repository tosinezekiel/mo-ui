<template>
    <div>
        <ProductListBanner />
        <main class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">

            <div class="pt-12 lg:grid lg:grid-cols-3 lg:gap-x-8 xl:grid-cols-4">
              <aside>
                <h2 class="sr-only">Filters</h2>

                <button type="button" class="inline-flex items-center lg:hidden" @click="mobileFiltersOpen = true">
                  <span class="text-sm font-medium text-gray-700">Filters</span>
                  <PlusIcon class="ml-1 h-5 w-5 flex-shrink-0 text-gray-400" aria-hidden="true" />
                </button>

                <div class="hidden lg:block">
                  <form class="space-y-10 divide-y divide-gray-200">
                    <div v-for="(section, sectionIdx) in filters" :key="section.name" :class="sectionIdx === 0 ? null : 'pt-10'">
                      <fieldset>
                        <legend class="block text-sm font-medium text-gray-900">{{ section.name }}</legend>
                        <div class="space-y-3 pt-6">
                          <div v-for="(option, optionIdx) in section.options" :key="option.value" class="flex items-center">
                            <input :id="`${section.id}-${optionIdx}`" :name="`${section.id}[]`" :value="option.value" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-500" />
                            <label :for="`${section.id}-${optionIdx}`" class="ml-3 text-sm text-gray-600">{{ option.label }}</label>
                          </div>
                        </div>
                      </fieldset>
                    </div>
                  </form>
                </div>
              </aside>
              <div class="mt-6 lg:col-span-2 lg:mt-0 xl:col-span-3">
                <CommonProductList title="Search results." subtitle="Three (3) items matched your search."/>
              </div>
            </div>
          </main>
        <AppFooter />
    </div>
</template>
<script setup>
import { ref } from 'vue'
import {
  Dialog,
  DialogPanel,
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
  TransitionChild,
  TransitionRoot,
} from '@headlessui/vue'
import { XMarkIcon } from '@heroicons/vue/24/outline'
import { ChevronDownIcon, PlusIcon } from '@heroicons/vue/24/solid'

const filters = [
  {
    id: 'collections',
    name: 'Collections',
    options: [
      { value: 'programming', label: 'Programming' },
      { value: 'cyber-security', label: 'Cyber Security' },
      { value: 'visual-design', label: 'Visual Design' },
      { value: 'data-analyst', label: 'Data Analyst' },
      { value: 'copywriting', label: 'Copy Writing' },
      { value: 'product-design', label: 'Product Design' },
      { value: 'abstract', label: 'Abstract' },
    ],
  },
  {
    id: 'category',
    name: 'Category',
    options: [
      { value: 'new-designs', label: 'New Designs' },
      { value: 'accessories', label: 'Tees' },
      { value: 'sweatshirts', label: 'Sweatshirts' },
      { value: 'pants-shorts', label: 'Pants & Shorts' },
    ],
  },
  {
    id: 'color',
    name: 'Color',
    options: [
      { value: 'white', label: 'White' },
      { value: 'beige', label: 'Beige' },
      { value: 'blue', label: 'Blue' },
      { value: 'brown', label: 'Brown' },
      { value: 'green', label: 'Green' },
      { value: 'purple', label: 'Purple' },
    ],
  },
  {
    id: 'sizes',
    name: 'Sizes',
    options: [
      { value: 'xs', label: 'XS' },
      { value: 's', label: 'S' },
      { value: 'm', label: 'M' },
      { value: 'l', label: 'L' },
      { value: 'xl', label: 'XL' },
      { value: '2xl', label: '2XL' },
    ],
  },
]

const mobileFiltersOpen = ref(false)
</script>