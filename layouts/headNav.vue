<template>
  <div>
    <header class="sm:px-4 sm:py-3 bg-gray-900 sm:flex sm:justify-between sm:items-center">
      <div class="px-4 py-3 sm:p-0 flex justify-between items-center">
        <nuxt-link to="/">
          <img class="h-8" src="~assets/logo.png" alt="brand logo" />
        </nuxt-link>
        <div class="sm:hidden">
          <svg
            @click="isOpen=!isOpen"
            viewBox="0 0 20 20"
            fill="currentColor"
            class="dots-horizontal w-6 h-6 text-gray-200"
          >
            <path
              v-if="!isOpen"
              d="M6 10a2 2 0 11-4 0 2 2 0 014 0zM12 10a2 2 0 11-4 0 2 2 0 014 0zM16 12a2 2 0 100-4 2 2 0 000 4z"
            />
            <path
              v-if="isOpen"
              d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
            />
          </svg>
        </div>
      </div>
      <div class="sm:block" :class="isOpen? 'block' :'hidden'">
        <div class="px-2 py-2 sm:p-0 sm:flex items-center text-gray-200">
          <nuxt-link
            to="/"
            class="px-2 py-1 sm:ml-2 block hover:bg-gray-800 font-semibold rounded"
            href="#"
          >Home</nuxt-link>
          <nuxt-link
            to="/property"
            class="px-2 py-1 block hover:bg-gray-800 font-semibold rounded"
            href="#"
          >Property Listing</nuxt-link>
          <nuxt-link
            to="/locations"
            class="px-2 py-1 sm:ml-2 block hover:bg-gray-800 font-semibold rounded"
            href="#"
          >Vacation</nuxt-link>
          <AccoutDropdown class="sm:ml-4 px-2 py-1 hidden sm:block" />
        </div>
        <div class="block sm:hidden border-t border-gray-800">
          <div class="mt-3 px-4 py-2">
            <div class="flex items-center">
              <img
                class="h-10 w-10 rounded-full border-2 border-gray-500 object-cover"
                src="~assets/talin.jpg"
                alt="profile picture"
              />
              <span class="ml-4 font-semibold text-gray-400">Milan Budhathoki</span>
            </div>
            <div class="mt-2">
              <a href="#" class="block py-1 text-gray-500 hover:text-gray-300">Account Settings</a>
              <a href="#" class="block py-1 text-gray-500 hover:text-gray-300">Support</a>
              <a href="#" class="block py-1 text-gray-500 hover:text-gray-300">Sign Out</a>
            </div>
          </div>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>

<style>
</style>