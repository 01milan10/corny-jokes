<template>
  <div class="relative">
    <button
      class="relative z-10 block h-10 w-10 rounded-full overflow-hidden border-2 border-gray-500 focus:outline-none focus:border-gray-200"
      @click="isOpen=!isOpen"
    >
      <img class="h-full w-full object-cover" src="~assets/talin.jpg" alt="profile picture" />
    </button>
    <button
      v-if="isOpen"
      tabindex="-1"
      @click="isOpen=false"
      class="fixed w-full h-full inset-0 bg-gray-900 opacity-50 cursor-default"
    ></button>
    <div
      class="absolute top-auto lg:z-10 right-0 mt-2 w-48 bg-white rounded-lg py-2 shadow-2xl"
      :class="isOpen?'block':'hidden'"
    >
      <a
        href="#"
        class="block px-4 py-2 text-gray-800 hover:bg-brand-blue hover:text-white"
      >Account Settings</a>
      <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-brand-blue hover:text-white">Support</a>
      <a
        href="#"
        class="block px-4 py-2 text-gray-800 hover:bg-brand-blue hover:text-white"
      >Sign Out</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  mounted() {
    const handleEscape = (e) => {
      if (e.key === "Esc" || e.key === "Escape") {
        this.isOpen = false;
      }
    };

    document.addEventListener("keydown", handleEscape);

    this.$once("hook:beforeDestroy", () => {
      document.removeEventListener("keydown", handleEscape);
    });
  },
};
</script>

<style>
</style>