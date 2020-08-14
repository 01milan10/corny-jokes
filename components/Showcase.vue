<template>
  <div class="flex bg-gray-800">
    <div class="px-4 py-6 max-w-md mx-auto sm:max-w-xl lg:max-w-full lg:w-1/2 lg:py-24 lg:px-12">
      <div class="xl:max-w-lg xl:ml-auto">
        <img
          class="mt-5 rounded-lg shadow-xl sm:mt-8 sm:w-full sm:object-cover sm:object-center lg:hidden"
          src="~/assets/workcation.jpg"
          alt="woman working"
        />
        <h1
          class="mt-5 text-2xl font-bold text-gray-300 leading-tight sm:mt-8 sm:text-4xl lg:text-3xl xl:text-4xl"
        >
          You can work from anywhere.
          <br class="sm:hidden lg:inline" />
          <span class="text-brand-blue">Take advantage of it.</span>
        </h1>
        <p
          class="text-gray-500 font-light mt-2 sm:mt-4 sm:text-xl"
        >Workacation helps you find work-friendly rentals in beautiful locations so you can enjoy some nice weather even when you're not on vacation.</p>
        <div class="mt-5 sm:mt-6">
          <a href="#" class="btn">Book your escape</a>
        </div>
      </div>
    </div>
    <div class="hidden lg:block lg:w-1/2">
      <img
        class="w-full h-full object-cover object-center"
        src="~/assets/workcation.jpg"
        alt="woman working"
      />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>