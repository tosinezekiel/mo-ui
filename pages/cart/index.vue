<template>
  <div class="bg-white">
    <AppNav> </AppNav>
    <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
      <h1 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
        Cart
      </h1>
      <small class="text-xs">You have four (4) items in your cart.</small>

      <form class="mt-12">
        <section aria-labelledby="cart-heading">
          <h2 id="cart-heading" class="sr-only">Items in your shopping cart</h2>

          <ul
            role="list"
            class="divide-y divide-gray-200 border-b border-t border-gray-200"
          >
            <li v-for="product in products" :key="product.id" class="flex py-6">
              <div class="flex-shrink-0">
                <img
                  :src="product.imageSrc"
                  :alt="product.imageAlt"
                  class="h-24 w-24 rounded-md object-cover object-center sm:h-32 sm:w-32"
                />
              </div>

              <div class="ml-4 flex flex-1 flex-col sm:ml-6">
                <div>
                  <div class="flex justify-between">
                    <h4 class="text-sm">
                      <a
                        :href="product.href"
                        class="font-medium text-gray-700 hover:text-gray-800"
                        >{{ product.name }}</a
                      >
                    </h4>
                    <div
                      class="flex items-center sm:block sm:flex-none sm:text-center"
                    >
                      <label :for="`quantity-${product.name}`" class="sr-only"
                        >Quantity, {{ product.name }}</label
                      >
                      <select
                        :id="`quantity-${product.id}`"
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
                    <p class="ml-4 text-sm font-medium text-gray-900">
                      {{ product.price }}
                    </p>
                  </div>
                  <p class="mt-1 text-sm text-gray-500">{{ product.color }}</p>
                  <p class="mt-1 text-sm text-gray-500">{{ product.size }}</p>
                  <div class="mt-4">
                    <button
                      type="button"
                      class="text-sm font-medium text-red-300 hover:text-red-400"
                    >
                      <span>Remove</span>
                    </button>
                  </div>
                </div>
              </div>
            </li>
          </ul>
        </section>

        <section
          aria-labelledby="summary-heading"
          class="mt-10 flex justify-between items-start"
        >
          <h2 id="summary-heading" class="sr-only">Order summary</h2>
          <div class="text-center text-sm">
            <p>
              <a
                href="#"
                class="font-medium text-yellow-500 hover:text-yellow-600"
              >
                <span aria-hidden="true"> &larr;</span>
                Continue Shopping
              </a>
            </p>
          </div>
          <div>
            <dl class="space-y-4">
              <div class="flex items-center justify-between">
                <dt class="text-base font-medium text-gray-900">Subtotal</dt>
                <dd class="ml-4 text-base font-medium text-gray-900">$96.00</dd>
              </div>
            </dl>
            <p class="mt-1 text-sm text-gray-500">
              Shipping and taxes will be calculated at checkout.
            </p>
            <div class="mt-2">
              <div>
                <div class="flex rounded-md shadow-sm">
                  <div
                    class="relative flex flex-grow items-stretch focus-within:z-10"
                  >
                    <div
                      class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-3"
                    ></div>
                    <input
                      type="text"
                      name="coupon"
                      id="coupon"
                      class="block w-full rounded-none rounded-l-md border-0 py-1.5 pl-10 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-yellow-600 sm:text-sm sm:leading-6"
                      placeholder="Enter promo code"
                    />
                  </div>
                  <button
                    type="button"
                    class="relative -ml-px inline-flex items-center gap-x-1.5 rounded-r-md px-3 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-yellow-50"
                  >
                    Apply
                  </button>
                </div>
              </div>
            </div>
            <div class="mt-2">
              <button
                type="submit"
                class="w-full rounded-md border border-transparent bg-gray-900 px-4 py-3 text-base font-medium text-white shadow-sm hover:bg-gray-800 focus:outline-none focus:ring-2 focus:ring-gray-600 focus:ring-offset-2 focus:ring-offset-gray-50"
              >
                Proceed to checkout
              </button>
            </div>
          </div>
        </section>
      </form>
    </div>
    <AppFooter />
  </div>
</template>

<script setup>
import { CheckIcon, ClockIcon } from "@heroicons/vue/20/solid";

const products = [
  {
    id: 1,
    name: "Artwork Tee",
    href: "#",
    price: "$32.00",
    color: "Mint",
    size: "M",
    inStock: true,
    imageSrc:
      "https://tailwindui.com/img/ecommerce-images/checkout-page-03-product-04.jpg",
    imageAlt: "Front side of mint cotton t-shirt with wavey lines pattern.",
  },
  {
    id: 2,
    name: "Basic Tee",
    href: "#",
    price: "$32.00",
    color: "Charcoal",
    inStock: false,
    leadTime: "7-8 years",
    size: "L",
    imageSrc:
      "https://tailwindui.com/img/ecommerce-images/shopping-cart-page-01-product-02.jpg",
    imageAlt: "Front side of charcoal cotton t-shirt.",
  },
];
</script>
