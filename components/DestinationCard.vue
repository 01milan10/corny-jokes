<template>
  <div class="p-8">
    <div class="flex flex-wrap justify-around">
      <div class="max-w-md m-4" v-for="destination in popularDestinations" :key="destination.city">
        <div class="shadow-lg">
          <img
            class="rounded-lg overflow-hidden object-cover"
            :src="require(`~/assets/img/${destination.imageUrl}`)"
            :alt="destination.imageAlt"
          />
        </div>
        <div class="relative -mt-10 px-4">
          <div class="z-10 px-5 py-2 bg-white rounded-lg shadow-2xl">
            <span class="block text-lg font-semibold text-gray-800">{{destination.city}}</span>
            <span class="block text-gray-800">
              ${{destination.averagePrice}}
              <span class="text-sm text-gray-600">/night</span>
            </span>
            <span
              class="block mt-4 text-indigo-500"
            >Explore {{destination.propertyCount}} properties</span>
            <div class="mt-1 flex items-baseline">
              <svg
                v-for="i in 5"
                :key="i"
                viewBox="0 0 20 20"
                fill="currentColor"
                :class="i <=destination.rating ? 'text-teal-500' : 'text-gray-400'"
                class="star w-4 h-4"
              >
                <path
                  d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"
                />
              </svg>
              <span class="ml-2 text-sm text-gray-700">{{destination.reviewsCount}} reviews</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      popularDestinations: [
        {
          city: "Toronto",
          averagePrice: 120,
          propertyCount: 76,
          imageUrl: "Toronto.jpg",
          imageAlt: "Toronto skyline",
          rating: 4,
          reviewsCount: 49,
        },
        {
          city: "Malibu",
          averagePrice: 215,
          propertyCount: 43,
          imageUrl: "Malibu.jpg",
          imageAlt: "Cliff in Malibu",
          rating: 4,
          reviewsCount: 49,
        },
        {
          city: "Chicago",
          averagePrice: 130,
          propertyCount: 115,
          imageUrl: "Chicago.jpg",
          imageAlt: "Chicago skyline",
          rating: 4,
          reviewsCount: 49,
        },
        {
          city: "Seattle",
          averagePrice: 135,
          propertyCount: 63,
          imageUrl: "Seattle.jpg",
          imageAlt: "Seattle skyline",
          rating: 4,
          reviewsCount: 49,
        },
        {
          city: "Colorado",
          averagePrice: 85,
          propertyCount: 47,
          imageUrl: "Colorado.jpg",
          imageAlt: "Lake in Colorado",
          rating: 4,
          reviewsCount: 49,
        },
        {
          city: "Miami",
          averagePrice: 115,
          propertyCount: 86,
          imageUrl: "Miami.jpg",
          imageAlt: "Beach in Miami",
          rating: 4,
          reviewsCount: 49,
        },
      ],
    };
  },
};
</script>

<style >
</style>