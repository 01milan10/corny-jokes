<template>
  <div>
    <div class="p-8">
      <PropertyCard :property="property" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      property: {
        imageUrl: "hotel-room.jpg",
        imageAlt: "Rear view of modern home with pool",
        beds: 3,
        baths: 2,
        title: "Modern home in Los Angeles",
        priceInCents: 190000,
        formattedPrice: "$1,900.00",
        reviewCount: 34,
        rating: 4,
      },
    };
  },
};
</script>

<style>
</style>