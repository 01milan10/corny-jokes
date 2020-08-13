<template>
  <div>
    <div class="max-w-md">
      <div>
        <img
          class="h-full w-full object-cover rounded-lg shadow-lg"
          :src="require(`~/assets/${property.imageUrl}`)"
          :alt="property.imageAlt"
        />
      </div>
      <div class="relative px-4 -mt-10">
        <div class="p-6 bg-gray-700 rounded-lg shadow-2xl">
          <div class="flex items-baseline">
            <span
              class="inline-block bg-teal-200 text-teal-800 text-xs px-2 rounded-full uppercase font-semibold tracking-wide"
            >New</span>
            <div
              class="ml-2 text-gray-500 text-xs uppercase font-semibold tracking-wide"
            >{{property.beds}} beds &bull; {{property.baths}} baths</div>
          </div>
          <h4 class="mt-1 font-semibold text-lg leading-tight text-gray-300">{{property.title}}</h4>
          <div class="mt-1 text-gray-500">
            {{property.formattedPrice}}
            <span class="text-gray-600">/ wk</span>
          </div>
          <div class="mt-2 flex items-center">
            <svg
              v-for="i in 5"
              :key="i"
              viewBox="0 0 20 20"
              fill="currentColor"
              :class="i <=property.rating ? 'text-teal-500' : 'text-gray-400'"
              class="star w-4 h-4"
            >
              <path
                d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"
              />
            </svg>
            <span class="ml-2 text-gray-500 text-sm">{{property.reviewCount}} reviews</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["property"],
};
</script>

<style>
</style> 