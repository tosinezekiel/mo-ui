<script setup>
import { EnvelopeIcon, LockClosedIcon } from "@heroicons/vue/24/outline";
</script>
<template>
  <div
    class="flex min-h-full flex-1 flex-col justify-center px-6 py-12 lg:px-8"
  >
    <div class="sm:mx-auto sm:w-full sm:max-w-sm">
      <h3
        class="mt-10 text-center text-4xl leading-9 tracking-tight text-gray-900"
      >
        Login
      </h3>
      <AuthSocialProviderIcons />
    </div>

    <div class="sm:mx-auto sm:w-full sm:max-w-sm">
      <form class="space-y-6" action="#" method="POST">
        <div class="relative">
          <EnvelopeIcon
            class="absolute left-3 top-1/2 transform -translate-y-1/2 h-5 w-5 text-gray-400"
          />
          <div class="mt-2">
            <input
              id="email"
              name="email"
              type="email"
              autocomplete="email"
              placeholder="Email"
              class="block w-full rounded-md border-0 py-2.5 pl-10 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-100 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-yellow-300 sm:text-sm sm:leading-6"
            />
          </div>
        </div>

        <div class="relative">
          <LockClosedIcon
            class="absolute left-3 top-1/2 transform -translate-y-1/2 h-5 w-5 text-gray-400"
          />
          <div class="mt-2">
            <input
              id="password"
              name="password"
              type="password"
              autocomplete="current-password"
              placeholder="Password"
              class="block w-full rounded-md border-0 py-2.5 pl-10 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-100 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-yellow-300 sm:text-sm sm:leading-6"
            />
          </div>
        </div>

        <div class="text-center">
          <p class="font-light">
            Don't have an account?
            <NuxtLink
              to="/account/register"
              class="font-semibold text-yellow-600 hover:text-yellow-500"
              >Sign up now?</NuxtLink
            >
          </p>
          <div class="text-sm">
            <NuxtLink
              to="#"
              class="font-semibold text-yellow-600 hover:text-yellow-500"
              >Forgot password?</NuxtLink
            >
          </div>
        </div>

        <div>
          <button
            type="submit"
            class="flex w-full justify-center rounded-md bg-yellow-500 px-3 py-2.5 pl-10 text-sm font-semibold leading-6 text-white shadow-sm hover:bg-yellow-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-yellow-600"
          >
            Sign in
          </button>
        </div>
      </form>
    </div>
  </div>
</template>
