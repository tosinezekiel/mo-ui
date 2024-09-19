<script setup lang="ts"></script>
<template>
  <div
    class="bg-footer flex min-h-screen flex-col items-center pt-48 space-y-48 text-white"
  >
    <div class="flex relative rounded-md overflow-hidden w-1/3">
      <input
        type="text"
        class="flex-grow px-4 py-3 rounded-full focus:outline-none"
        placeholder="Please enter your email address"
      />
      <button
        class="z-10 px-4 py-3 bg-gray-800 text-white font-bold absolute right-0 rounded-full hover:bg-gray-700 w-48"
      >
        Subscribe
      </button>
    </div>
    <div class="flex flex-col justify-center items-center space-y-2">
      <img
        src="/images/modesigno-web.svg"
        alt="Modesigno"
        width="200"
        height="80"
      />
      <h2 class="text-lg">creative@modesigno.com</h2>
      <div class="flex justify-between w-12">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="white"
          viewBox="0 0 24 24"
        >
          <path
            d="M7 2C4.239 2 2 4.239 2 7v10c0 2.761 2.239 5 5 5h10c2.761 0 5-2.239 5-5V7c0-2.761-2.239-5-5-5H7zm8 3a1 1 0 1 1 0 2 1 1 0 0 1 0-2zm-3 3c2.209 0 4 1.791 4 4s-1.791 4-4 4-4-1.791-4-4 1.791-4 4-4zm8 10c0 .552-.448 1-1 1H5c-.552 0-1-.448-1-1v-4.819c.329.11.676.159 1.023.143h.601c-.161.484-.241 1.005-.232 1.536.024 1.384.574 2.678 1.512 3.617C8.349 20.863 10.125 21.5 12 21.5s3.651-.637 4.59-1.576c.94-.939 1.49-2.233 1.514-3.617.01-.531-.071-1.052-.232-1.536h.601c.347.016.694-.033 1.023-.143V17z"
          />
        </svg>

        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="white"
          viewBox="0 0 24 24"
        >
          <path
            d="M12 2C6.477 2 2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.879V14.89h-2.32v-2.89h2.32V9.8c0-2.31 1.412-3.578 3.473-3.578.986 0 1.834.073 2.082.106v2.418l-1.428.001c-1.118 0-1.334.532-1.334 1.312v1.721h2.662l-.347 2.89h-2.315v7.989C18.343 21.128 22 16.991 22 12c0-5.523-4.477-10-10-10z"
          />
        </svg>
      </div>
    </div>
    <div class="text-lg">
      <span>copyright &copy; 2021</span>
    </div>
  </div>
</template>


<style scoped>
.bg-footer {
  background: url('/images/footer-bg.png');
  background-position: center;
  background-size: cover;
}
</style>
