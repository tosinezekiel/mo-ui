<template>
  <form>
    <div>
      <h2 class="text-lg font-medium text-gray-900">Contact information</h2>

      <div class="mt-4">
        <label
          for="email-address"
          class="block text-sm font-medium text-gray-700"
          >Email address</label
        >
        <div class="mt-1">
          <input
            type="email"
            id="email-address"
            name="email-address"
            autocomplete="email"
            class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
          />
        </div>
      </div>
    </div>

    <div class="mt-10 border-t border-gray-200 pt-10">
      <h2 class="text-lg font-medium text-gray-900">Billing information</h2>
      <small class="text-xs text-gray-400"
        >Please ensure the information provided below are accurate.</small
      >

      <div class="mt-4 grid grid-cols-1 gap-y-6 sm:grid-cols-2 sm:gap-x-4">
        <div>
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
            >First name</label
          >
          <div class="mt-1">
            <input
              type="text"
              id="first-name"
              name="first-name"
              autocomplete="given-name"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div>
          <label for="last-name" class="block text-sm font-medium text-gray-700"
            >Last name</label
          >
          <div class="mt-1">
            <input
              type="text"
              id="last-name"
              name="last-name"
              autocomplete="family-name"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div class="sm:col-span-2">
          <label for="address" class="block text-sm font-medium text-gray-700"
            >Address</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="address"
              id="address"
              autocomplete="street-address"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div class="sm:col-span-2">
          <label for="apartment" class="block text-sm font-medium text-gray-700"
            >Apartment, suite, etc.</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="apartment"
              id="apartment"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div>
          <label for="city" class="block text-sm font-medium text-gray-700"
            >City</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="city"
              id="city"
              autocomplete="address-level2"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div>
          <label for="country" class="block text-sm font-medium text-gray-700"
            >Country</label
          >
          <div class="mt-1">
            <select
              id="country"
              name="country"
              autocomplete="country-name"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            >
              <option>United States</option>
              <option>Canada</option>
              <option>Mexico</option>
            </select>
          </div>
        </div>

        <div>
          <label for="region" class="block text-sm font-medium text-gray-700"
            >State / Province</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="region"
              id="region"
              autocomplete="address-level1"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div>
          <label
            for="postal-code"
            class="block text-sm font-medium text-gray-700"
            >Postal code</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="postal-code"
              id="postal-code"
              autocomplete="postal-code"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div class="sm:col-span-2">
          <label for="phone" class="block text-sm font-medium text-gray-700"
            >Phone</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="phone"
              id="phone"
              autocomplete="tel"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>
      </div>
    </div>

    <div class="mt-10 border-t border-gray-200 pt-10">
      <h2 class="text-lg font-medium text-gray-900">Shipping information</h2>
      <small class="text-xs text-gray-400"
        >Please provide accurate information about where this order would be
        received.</small
      >

      <div class="mt-4 grid grid-cols-1 gap-y-6 sm:grid-cols-2 sm:gap-x-4">
        <div>
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
            >First name</label
          >
          <div class="mt-1">
            <input
              type="text"
              id="first-name"
              name="first-name"
              autocomplete="given-name"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div>
          <label for="last-name" class="block text-sm font-medium text-gray-700"
            >Last name</label
          >
          <div class="mt-1">
            <input
              type="text"
              id="last-name"
              name="last-name"
              autocomplete="family-name"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div class="sm:col-span-2">
          <label for="company" class="block text-sm font-medium text-gray-700"
            >Company (optional)</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="company"
              id="company"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div class="sm:col-span-2">
          <label for="address" class="block text-sm font-medium text-gray-700"
            >Address</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="address"
              id="address"
              autocomplete="street-address"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div class="sm:col-span-2">
          <label for="apartment" class="block text-sm font-medium text-gray-700"
            >Apartment, suite, etc.</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="apartment"
              id="apartment"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div>
          <label for="city" class="block text-sm font-medium text-gray-700"
            >City</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="city"
              id="city"
              autocomplete="address-level2"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div>
          <label for="country" class="block text-sm font-medium text-gray-700"
            >Country</label
          >
          <div class="mt-1">
            <select
              id="country"
              name="country"
              autocomplete="country-name"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            >
              <option>United States</option>
              <option>Canada</option>
              <option>Mexico</option>
            </select>
          </div>
        </div>

        <div>
          <label for="region" class="block text-sm font-medium text-gray-700"
            >State / Province</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="region"
              id="region"
              autocomplete="address-level1"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div>
          <label
            for="postal-code"
            class="block text-sm font-medium text-gray-700"
            >Postal code</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="postal-code"
              id="postal-code"
              autocomplete="postal-code"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div class="sm:col-span-2">
          <label for="phone" class="block text-sm font-medium text-gray-700"
            >Phone</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="phone"
              id="phone"
              autocomplete="tel"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>
      </div>
    </div>

    <div class="mt-10 border-t border-gray-200 pt-10">
      <h2 class="text-lg font-medium text-gray-900">Delivery method</h2>
      <small class="text-xs text-gray-400"
        >Please select either of the delivery methods below.</small
      >

      <fieldset aria-label="Delivery method" class="mt-4">
        <RadioGroup
          v-model="selectedDeliveryMethod"
          class="grid grid-cols-1 gap-y-6 sm:grid-cols-2 sm:gap-x-4"
        >
          <RadioGroupOption
            as="template"
            v-for="deliveryMethod in deliveryMethods"
            :key="deliveryMethod.id"
            :value="deliveryMethod"
            :aria-label="deliveryMethod.title"
            :aria-description="`${deliveryMethod.turnaround} for ${deliveryMethod.price}`"
            v-slot="{ active, checked }"
          >
            <div
              :class="[
                checked ? 'border-transparent' : 'border-gray-300',
                active ? 'ring-2 ring-yellow-500' : '',
                'relative flex cursor-pointer rounded-lg border bg-white p-4 shadow-sm focus:outline-none',
              ]"
            >
              <span class="flex flex-1">
                <span class="flex flex-col">
                  <span class="block text-sm font-medium text-gray-900">{{
                    deliveryMethod.title
                  }}</span>
                  <span class="mt-1 flex items-center text-sm text-gray-500">{{
                    deliveryMethod.turnaround
                  }}</span>
                  <span class="mt-6 text-sm font-medium text-gray-900">{{
                    deliveryMethod.price
                  }}</span>
                </span>
              </span>
              <CheckCircleIcon
                v-if="checked"
                class="h-5 w-5 text-yellow-600"
                aria-hidden="true"
              />
              <span
                :class="[
                  active ? 'border' : 'border-2',
                  checked ? 'border-yellow-500' : 'border-transparent',
                  'pointer-events-none absolute -inset-px rounded-lg',
                ]"
                aria-hidden="true"
              />
            </div>
          </RadioGroupOption>
        </RadioGroup>
      </fieldset>
    </div>

    <!-- Payment -->
    <div class="mt-10 border-t border-gray-200 pt-10">
      <h2 class="text-lg font-medium text-gray-900">Payment Method</h2>
      <small class="text-xs text-gray-400"
        >Please select either of the payment methods below.</small
      >

      <fieldset aria-label="Payment method" class="mt-4">
        <RadioGroup
          v-model="selectedPayment"
          class="grid grid-cols-1 gap-y-6 sm:grid-cols-2 sm:gap-x-4"
        >
          <RadioGroupOption
            as="template"
            v-for="paymentMethod in paymentMethods"
            :key="paymentMethod.id"
            :value="paymentMethod"
            :aria-label="paymentMethod.title"
            :disabled="!paymentMethod.isActive"
            v-slot="{ active, checked, disabled }"
          >
            <div
              :class="[
                checked ? 'border-transparent' : 'border-gray-300',
                active ? 'ring-2 ring-yellow-500' : '',
                disabled ? 'opacity-50 cursor-not-allowed' : 'cursor-pointer',
                'relative flex cursor-pointer rounded-lg border bg-white p-4 shadow-sm focus:outline-none',
              ]"
            >
              <div
                v-if="!paymentMethod.isActive"
                class="absolute top-0 right-0 bg-yellow-500 text-white text-xs font-semibold px-2 py-1 rounded-bl-lg rounded-tr-lg"
              >
                Coming Soon
              </div>
              <font-awesome-icon
                :icon="paymentMethod.icon"
                :class="[
                  checked ? 'text-yellow-400' : '',
                  'text-3xl mr-4 w-4 h-4 self-center text-gray-400',
                ]"
              />
              <span class="flex flex-1">
                <span class="flex flex-col">
                  <span class="block text-sm font-medium text-gray-900">
                    {{ paymentMethod.title }}
                  </span>
                </span>
              </span>

              <CheckCircleIcon
                v-if="checked"
                class="h-5 w-5 text-yellow-600"
                aria-hidden="true"
              />

              <span
                :class="[
                  active ? 'border' : 'border-2',
                  checked ? 'border-yellow-500' : 'border-transparent',
                  'pointer-events-none absolute -inset-px rounded-lg',
                ]"
                aria-hidden="true"
              />
            </div>
          </RadioGroupOption>
        </RadioGroup>
      </fieldset>

      <div class="mt-6 grid grid-cols-4 gap-x-4 gap-y-6">
        <div class="col-span-4">
          <label
            for="card-number"
            class="block text-sm font-medium text-gray-700"
            >Card number</label
          >
          <div class="mt-1">
            <input
              type="text"
              id="card-number"
              name="card-number"
              autocomplete="cc-number"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div class="col-span-4">
          <label
            for="name-on-card"
            class="block text-sm font-medium text-gray-700"
            >Name on card</label
          >
          <div class="mt-1">
            <input
              type="text"
              id="name-on-card"
              name="name-on-card"
              autocomplete="cc-name"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div class="col-span-3">
          <label
            for="expiration-date"
            class="block text-sm font-medium text-gray-700"
            >Expiration date (MM/YY)</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="expiration-date"
              id="expiration-date"
              autocomplete="cc-exp"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>

        <div>
          <label for="cvc" class="block text-sm font-medium text-gray-700"
            >CVC</label
          >
          <div class="mt-1">
            <input
              type="text"
              name="cvc"
              id="cvc"
              autocomplete="csc"
              class="block w-full rounded-md border-gray-300 shadow-sm focus:border-yellow-500 focus:ring-yellow-500 sm:text-sm"
            />
          </div>
        </div>
      </div>
    </div>

    <div
      class="fixed bottom-0 left-0 w-full bg-white border-t border-gray-200 p-4"
    >
      <div
        class="flex items-center justify-between border-t border-gray-200 px-4 py-6 sm:px-6"
      >
        <!-- Total -->
        <div class="flex flex-col items-start">
          <dt class="text-base font-medium">Total</dt>
          <dd class="text-base font-medium text-gray-900">$75.52</dd>
        </div>

        <div class="ml-auto">
          <button
            type="submit"
            class="w-full rounded-md border border-transparent bg-gray-900 px-6 py-3 text-base font-medium text-white shadow-sm hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-gray-500 focus:ring-offset-2 focus:ring-offset-gray-50"
          >
            Proceed to payment
          </button>
        </div>
      </div>
    </div>
  </form>
</template>
<script setup>
import {
  Dialog,
  DialogPanel,
  Popover,
  PopoverButton,
  PopoverGroup,
  PopoverPanel,
  RadioGroup,
  RadioGroupOption,
  Tab,
  TabGroup,
  TabList,
  TabPanel,
  TabPanels,
  TransitionChild,
  TransitionRoot,
} from "@headlessui/vue";
import {
  Bars3Icon,
  MagnifyingGlassIcon,
  QuestionMarkCircleIcon,
  ShoppingBagIcon,
  XMarkIcon,
} from "@heroicons/vue/24/outline";
import {
  CheckCircleIcon,
  ChevronDownIcon,
  TrashIcon,
} from "@heroicons/vue/20/solid";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

import { faPaypal } from '@fortawesome/free-brands-svg-icons' 
import { faCreditCard, faCoins } from '@fortawesome/free-solid-svg-icons'

import { library } from "@fortawesome/fontawesome-svg-core";

library.add(faPaypal, faCreditCard, faCoins);
import { ref } from "vue";
const deliveryMethods = [
  {
    id: 1,
    title: "Standard",
    turnaround: "4–10 business days",
    price: "$5.00",
  },
  { id: 2, title: "Express", turnaround: "2–5 business days", price: "$16.00" },
];
const paymentMethods = [
  {
    id: "paypal",
    title: "PayPal",
    icon: ["fab", "paypal"],
    isActive: true,
  },
  {
    id: "credit-card",
    title: "Credit Card",
    icon: ["fas", "credit-card"],
    isActive: true,
  },
  {
    id: "coin",
    title: "Coin",
    icon: ["fas", "coins"],
    isActive: false,
  },
];

const open = ref(false);
const selectedDeliveryMethod = ref(deliveryMethods[0]);
const selectedPayment = ref(paymentMethods[0]);
</script>
