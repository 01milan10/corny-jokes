<template>
  <div class="max-w-md sm:max-w-xl lg:max-w-6xl mx-auto px-8 lg:px-12 py-8">
    <div>
      <p class="font-semibold text-lg text-gray-800">Popular destinations</p>
      <p
        class="text-gray-700"
      >A selection of great work-friendly cities with lots to see and explore.</p>
    </div>
    <div class="flex flex-wrap">
      <div
        class="mt-6 px-3 w-full xl:w-1/3 lg:w-1/2"
        v-for="destination in popularDestinations"
        :key="destination.city"
      >
        <div class="flex items-center rounded-lg bg-white overflow-hidden shadow-2xl">
          <img
            class="h-32 w-32 object-cover"
            :src="require(`~/assets/img/${destination.imageUrl}`)"
            :alt="popularDestinations.imageAlt"
          />
          <div class="p-4 w-full">
            <span class="block font-semibold">{{destination.city}}</span>
            <span class="block pt-1">{{destination.averagePrice}} /night average</span>
            <a
              href="#"
              class="block mt-5 font-semibold text-sm text-indigo-600 hover:text-indigo-500"
            >Explore {{destination.propertyCount}} poperties</a>
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
        },
        {
          city: "Malibu",
          averagePrice: 215,
          propertyCount: 43,
          imageUrl: "Malibu.jpg",
          imageAlt: "Cliff in Malibu",
        },
        {
          city: "Chicago",
          averagePrice: 130,
          propertyCount: 115,
          imageUrl: "Chicago.jpg",
          imageAlt: "Chicago skyline",
        },
        {
          city: "Seattle",
          averagePrice: 135,
          propertyCount: 63,
          imageUrl: "Seattle.jpg",
          imageAlt: "Seattle skyline",
        },
        {
          city: "Colorado",
          averagePrice: 85,
          propertyCount: 47,
          imageUrl: "Colorado.jpg",
          imageAlt: "Lake in Colorado",
        },
        {
          city: "Miami",
          averagePrice: 115,
          propertyCount: 86,
          imageUrl: "Miami.jpg",
          imageAlt: "Beach in Miami",
        },
      ],
    };
  },
};
</script>

<style>
</style>