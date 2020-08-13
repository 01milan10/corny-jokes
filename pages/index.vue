<template>
  <div>
    <Showcase />
    <div>
      <div class="max-w-md sm:max-w-xl lg:max-w-6xl mx-auto px-8 lg:px-12 py-8">
        <h2 class="text-xl text-gray-900">Popular destinations</h2>
        <p
          class="text-gray-600"
        >A selection of great work-friendly cities with lots to see and explore.</p>
        <div class="flex flex-wrap -mx-4">
          <div
            class="mt-6 w-full px-4 lg:w-1/2 xl:w-1/3"
            v-for="destination in popularDestinations"
            :key="destination.city"
          >
            <Destinations :destination="destination" />
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
.btn {
  @apply bg-brand-blue text-sm text-white uppercase tracking-wider font-semibold px-5 py-3 rounded-lg shadow-lg;
}
.btn:hover {
  @apply bg-indigo-400;
}
.btn:focus {
  @apply outline-none shadow-outline;
}
.btn:active {
  @apply bg-indigo-600;
}
@screen sm {
  .btn {
    @apply text-base;
  }
}
</style>
