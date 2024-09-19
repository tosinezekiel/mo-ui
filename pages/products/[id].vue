<template>
  <div class="bg-white">
    <AppNav> </AppNav>
    <div
      class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8"
    >
      <div class="lg:grid lg:grid-cols-2 lg:items-start lg:gap-x-8">
        <TabGroup as="div" class="flex flex-col-reverse">
          <div
            class="mx-auto mt-6 hidden w-full max-w-2xl sm:block lg:max-w-none"
          >
            <TabList class="grid grid-cols-4 gap-6">
              <Tab
                v-for="image in product.images"
                :key="image.id"
                class="relative flex h-24 cursor-pointer items-center justify-center rounded-md bg-white text-sm font-medium uppercase text-gray-900 hover:bg-gray-50 focus:outline-none focus:ring focus:ring-opacity-50 focus:ring-offset-4"
                v-slot="{ selected }"
              >
                <span class="sr-only">{{ image.name }}</span>
                <span class="absolute inset-0 overflow-hidden rounded-md">
                  <img
                    :src="image.src"
                    alt=""
                    class="h-full w-full object-cover object-center"
                  />
                </span>
                <span
                  :class="[
                    selected ? 'ring-yellow-500' : 'ring-transparent',
                    'pointer-events-none absolute inset-0 rounded-md ring-2 ring-offset-2',
                  ]"
                  aria-hidden="true"
                />
              </Tab>
            </TabList>
          </div>

          <TabPanels class="aspect-h-1 aspect-w-1 w-full">
            <TabPanel v-for="image in product.images" :key="image.id">
              <img
                :src="image.src"
                :alt="image.alt"
                class="h-full w-full object-cover object-center sm:rounded-lg"
              />
            </TabPanel>
          </TabPanels>
        </TabGroup>

        <!-- Product info -->
        <div class="mt-10 px-4 sm:mt-16 sm:px-0 lg:mt-0">
          <h1 class="text-3xl font-bold tracking-tight text-gray-900">
            {{ product.name }}
          </h1>

          <div class="mt-3">
            <h3 class="sr-only">Reviews</h3>
            <div class="flex items-center">
              <div class="flex items-center">
                <StarIcon
                  v-for="rating in [0, 1, 2, 3, 4]"
                  :key="rating"
                  :class="[
                    product.rating > rating
                      ? 'text-yellow-500'
                      : 'text-gray-300',
                    'h-5 w-5 flex-shrink-0',
                  ]"
                  aria-hidden="true"
                />
              </div>
              <p class="sr-only">{{ product.rating }} out of 5 stars</p>
            </div>
          </div>

          <div class="mt-6">
            <h3 class="sr-only">Description</h3>

            <div
              class="space-y-6 text-base text-gray-700"
              v-html="product.description"
            />
          </div>

          <div class="mt-3">
            <h2 class="sr-only">Product information</h2>
            <p class="text-3xl tracking-tight text-gray-900">
              {{ product.price }}
            </p>
          </div>

          <form class="mt-6">
            <!-- Colors -->
            <div class="flex w-full">
              <div>
                <h3 class="text-sm font-medium text-gray-600">Color</h3>

                <fieldset aria-label="Choose a color" class="mt-2">
                  <RadioGroup
                    v-model="selectedColor"
                    class="grid grid-cols-4 gap-4"
                  >
                    <RadioGroupOption
                      as="template"
                      v-for="color in product.colors"
                      :key="color.name"
                      :value="color"
                      :aria-label="color.name"
                      v-slot="{ active, checked }"
                    >
                      <div
                        :class="[
                          color.selectedColor,
                          active && checked ? 'ring ring-offset-1' : '',
                          !active && checked ? 'ring-2' : '',
                          'relative flex cursor-pointer items-center justify-center rounded-full p-0.5 focus:outline-none',
                        ]"
                      >
                        <span
                          aria-hidden="true"
                          :class="[
                            color.bgColor,
                            'h-8 w-8 rounded-full border border-black border-opacity-10',
                          ]"
                        />
                      </div>
                    </RadioGroupOption>
                  </RadioGroup>
                </fieldset>
              </div>
              <div>
                <div class="flex items-center justify-between">
                  <h3 class="text-sm font-medium text-gray-900 ml-8">Size</h3>
                  <a
                    href="#"
                    class="text-sm font-medium text-yellow-600 hover:text-yellow-500"
                    >Size guide</a
                  >
                </div>

                <fieldset aria-label="Choose a size" class="mt-4 ml-8">
                  <RadioGroup
                    v-model="selectedSize"
                    class="grid grid-cols-4 gap-4"
                  >
                    <RadioGroupOption
                      as="template"
                      v-for="size in product.sizes"
                      :key="size.name"
                      :value="size"
                      :disabled="!size.inStock"
                      v-slot="{ active, checked }"
                    >
                      <div
                        :class="[
                          size.inStock
                            ? 'cursor-pointer bg-white text-gray-900 shadow-sm'
                            : 'cursor-not-allowed bg-gray-50 text-gray-200',
                          'relative flex items-center justify-center rounded-md border px-4 py-2 text-sm font-medium uppercase hover:bg-gray-50 focus:outline-none',
                        ]"
                      >
                        <span :class="[checked ? 'z-50 text-white' : '']">{{
                          size.name
                        }}</span>
                        <span
                          v-if="size.inStock"
                          :class="[
                            active ? 'border' : 'border-2',
                            checked ? 'bg-yellow-500' : 'border-transparent',
                            'pointer-events-none absolute -inset-px rounded-md',
                          ]"
                          aria-hidden="true"
                        />
                        <span
                          v-else
                          aria-hidden="true"
                          class="pointer-events-none absolute -inset-px rounded-md border-2 border-gray-200"
                        >
                          <svg
                            class="absolute inset-0 h-full w-full stroke-2 text-gray-200"
                            viewBox="0 0 100 100"
                            preserveAspectRatio="none"
                            stroke="currentColor"
                          >
                            <line
                              x1="0"
                              y1="100"
                              x2="100"
                              y2="0"
                              vector-effect="non-scaling-stroke"
                            />
                          </svg>
                        </span>
                      </div>
                    </RadioGroupOption>
                  </RadioGroup>
                </fieldset>
              </div>
            </div>

            <div class="mt-10 flex items-center">
              <div
                class="flex items-center sm:block sm:flex-none sm:text-center"
              >
                <label :for="`quantity-${product.name}`" class="sr-only"
                  >Quantity, {{ product.name }}</label
                >
                <select
                  :id="`quantity-${product.name}`"
                  :name="`quantity-${product.name}`"
                  class="block max-w-full rounded-md border border-gray-300 py-3 px-2.5 text-left text-base font-medium leading-5 text-gray-700 shadow-sm focus:border-yellow-500 focus:outline-none focus:ring-1 focus:ring-yellow-500 sm:text-sm"
                >
                  <option value="1">1</option>
                  <option value="2">2</option>
                  <option value="3">3</option>
                  <option value="4">4</option>
                  <option value="5">5</option>
                  <option value="6">6</option>
                  <option value="7">7</option>
                  <option value="8">8</option>
                </select>
              </div>
              <button
                type="submit"
                class="flex max-w-xs ml-4 flex-1 items-center justify-center rounded-md border border-transparent bg-yellow-600 px-8 py-3 text-base font-medium text-white hover:bg-yellow-700 focus:outline-none focus:ring-2 focus:ring-yellow-500 focus:ring-offset-2 focus:ring-offset-gray-50 sm:w-full"
              >
                Add to bag
              </button>

              <button
                type="button"
                class="ml-4 flex items-center justify-center rounded-md px-3 py-3 text-gray-400 hover:bg-gray-100 hover:text-gray-500"
              >
                <HeartIcon class="h-6 w-6 flex-shrink-0" aria-hidden="true" />
                <span class="sr-only">Add to favorites</span>
              </button>
              </div>
              <div class="flex items-center mt-5 ">
                <h6 class="text-sm">Share this product: <i class="fa-solid fa-camera"></i></h6>
                <div class="flex w-20 justify-between ml-3">
                  <font-awesome-icon :icon="['fab', 'facebook']" class="text-blue-600 text-sm" />
                  <font-awesome-icon :icon="['fab', 'instagram']" class="ml-3 text-pink-600 text-sm" />
                  <font-awesome-icon :icon="['fab', 'twitter']" class="ml-3 text-blue-400 text-sm" />
                  <font-awesome-icon :icon="['fab', 'whatsapp']" class="ml-3 text-green-500 text-sm" />
                  
                  <font-awesome-icon :icon="['fas', 'copy']" class="ml-3 text-gray-500 text-sm" />
                </div>
              </div>
          </form>
        </div>
      </div>

      <section class="mt-20 flex justify-center text-center">
        <div class="sm:hidden">
          <label for="tabs" class="sr-only">Select a tab</label>
          <select
            id="tabs"
            name="tabs"
            class="block w-full rounded-md border-gray-300 focus:border-yellow-500 focus:ring-yellow-500"
          >
            <option v-for="tab in tabs" :key="tab.name" :selected="tab.current">
              {{ tab.name }}
            </option>
          </select>
        </div>
        <div class="hidden sm:block">
          <nav class="flex space-x-4" aria-label="Tabs">
            <a
              v-for="tab in tabs"
              :key="tab.name"
              :href="tab.href"
              :class="[
                tab.current
                  ? 'bg-yellow-100 text-yellow-700'
                  : 'text-gray-500 hover:text-gray-700',
                'rounded-full px-3 py-2 text-sm font-medium',
              ]"
              :aria-current="tab.current ? 'page' : undefined"
              >{{ tab.name }}</a
            >
          </nav>
        </div>
      </section>

      <section class="mt-14 bg-white">
        <div>
          <h2 class="sr-only">Customer Reviews</h2>

          <div class="-my-10">
            <h2 class="font-semibold text-lg">Reviews</h2>
            <div
              v-for="(review, reviewIdx) in reviews"
              :key="review.id"
              class="bg-gray-100 px-10 rounded-lg flex space-x-4 justify-center text-sm text-gray-500 mb-5"
            >
              <div
                :class="[
                  reviewIdx === 0 ? '' : 'border-t border-gray-200',
                  'flex-1 py-10',
                ]"
              >
                <h3 class="font-medium text-gray-900">{{ review.author }}</h3>
                <p>
                  <time :datetime="review.datetime">{{ review.date }}</time>
                </p>
                <div class="mt-4 text-gray-500" v-html="review.content" />
                <div class="mt-4 flex items-center">
                  <StarIcon
                    v-for="rating in [0, 1, 2, 3, 4]"
                    :key="rating"
                    :class="[
                      review.rating > rating
                        ? 'text-yellow-400'
                        : 'text-gray-300',
                      'h-5 w-5 flex-shrink-0',
                    ]"
                    aria-hidden="true"
                  />
                </div>
                <p class="sr-only">{{ review.rating }} out of 5 stars</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="py-16 sm:py-24">
            <CommonProductList title="Good for you"/>
        </section>
    </div>
    <AppFooter />
  </div>
</template>

<script setup>
import { ref } from "vue";
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

import { faFacebook, faInstagram, faTwitter, faWhatsapp } from '@fortawesome/free-brands-svg-icons'
import { faCopy } from '@fortawesome/free-solid-svg-icons'

import { library } from '@fortawesome/fontawesome-svg-core'

library.add(faFacebook, faInstagram, faTwitter, faWhatsapp, faCopy)
import {
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
  RadioGroup,
  RadioGroupOption,
  Tab,
  TabGroup,
  TabList,
  TabPanel,
  TabPanels,
} from "@headlessui/vue";
import { StarIcon } from "@heroicons/vue/20/solid";
import { HeartIcon, MinusIcon, PlusIcon } from "@heroicons/vue/24/outline";

const tabs = [
  { name: "Product details", href: "#", current: false },
  { name: "Designer", href: "#", current: false },
  { name: "Reviews", href: "#", current: true },
];

const reviews = [
  {
    id: 1,
    rating: 5,
    content: `
      <p>This icon pack is just what I need for my latest project. There's an icon for just about anything I could ever need. Love the playful look!</p>
    `,
    date: "July 16, 2021",
    datetime: "2021-07-16",
    author: "Emily Selman",
  },
  {
    id: 2,
    rating: 5,
    content: `
      <p>Blown away by how polished this icon pack is. Everything looks so consistent and each SVG is optimized out of the box so I can use it directly with confidence. It would take me several hours to create a single icon this good, so it's a steal at this price.</p>
    `,
    date: "July 12, 2021",
    datetime: "2021-07-12",
    author: "Hector Gibbons",
  },
];

const product = {
  name: "Zip Tote Basket",
  price: "$140",
  rating: 4,
  images: [
    {
      id: 1,
      name: "Angled view",
      src: "https://tailwindui.com/img/ecommerce-images/product-page-03-product-01.jpg",
      alt: "Angled front view with bag zipped and handles upright.",
    },
    {
      id: 2,
      name: "Angled view",
      src: "https://tailwindui.com/img/ecommerce-images/product-page-03-product-01.jpg",
      alt: "Angled front view with bag zipped and handles upright.",
    },
    {
      id: 3,
      name: "Angled view",
      src: "https://tailwindui.com/img/ecommerce-images/product-page-03-product-01.jpg",
      alt: "Angled front view with bag zipped and handles upright.",
    },
    {
      id: 4,
      name: "Angled view",
      src: "https://tailwindui.com/img/ecommerce-images/product-page-03-product-01.jpg",
      alt: "Angled front view with bag zipped and handles upright.",
    },
  ],
  colors: [
    {
      name: "Washed Black",
      bgColor: "bg-gray-700",
      selectedColor: "ring-gray-700",
    },
    { name: "White", bgColor: "bg-white", selectedColor: "ring-gray-400" },
    {
      name: "Washed Gray",
      bgColor: "bg-gray-500",
      selectedColor: "ring-gray-500",
    },
    { name: "Red", bgColor: "bg-red-500", selectedColor: "ring-red-500" },
    {
      name: "Light Green",
      bgColor: "bg-green-500",
      selectedColor: "ring-green-500",
    },
    {
      name: "Purple",
      bgColor: "bg-yellow-500",
      selectedColor: "ring-yellow-500",
    },
    { name: "Brown", bgColor: "bg-blue-500", selectedColor: "ring-blue-500" },
  ],
  sizes: [
    { name: "XXS", inStock: false },
    { name: "XS", inStock: true },
    { name: "S", inStock: true },
    { name: "M", inStock: true },
    { name: "L", inStock: true },
    { name: "XL", inStock: true },
    { name: "2XL", inStock: true },
    { name: "3XL", inStock: true },
  ],
  description: `
    <p>The Zip Tote Basket is the perfect midpoint between shopping tote and comfy backpack. With convertible straps, you can hand carry, should sling, or backpack this convenient and spacious bag. The zip top and durable canvas construction keeps your goods protected for all-day use.</p>
  `,
  details: [
    {
      name: "Features",
      items: [
        "Multiple strap configurations",
        "Spacious interior with top zip",
        "Leather handle and tabs",
        "Interior dividers",
        "Stainless strap loops",
        "Double stitched construction",
        "Water-resistant",
      ],
    },
  ],
};

const selectedColor = ref(product.colors[0]);
const selectedSize = ref(product.sizes[2]);
</script>
