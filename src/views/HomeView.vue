<template>
  <div
    class="min-h-screen bg-cover bg-center flex items-center justify-center p-4"
    style="
      background-image: url('public/Pizza1.png');
    "
  >
    <div
      class="bg-black/80 px-8 py-10 rounded-2xl text-white text-center max-w-[90%]"
    >
      <h1 class="text-4xl md:text-6xl font-bold mb-4">Pizza Home</h1>
      <p class="text-red-500 text-xl md:text-2xl mb-3">
        Authentic Italian Pizza
      </p>
      <p class="text-gray-300 text-sm md:text-base">
        Fresh ingredients, dough made daily
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>
