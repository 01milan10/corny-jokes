<template>
  <div>
    <Showcase />
    <VisitLocation />
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
