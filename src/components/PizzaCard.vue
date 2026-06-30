<template>
  <div
    class="bg-red-200 p-6 rounded-xl text-center border-2 hover:border-black"
  >
    <h3 class="font-bold mb-2 text-black">{{ name }}</h3>
    <p class="text-black mb-3 text-sm">{{ description }}</p>
    <p class="text-red-500 font-bold text-lg">{{ price }} JD</p>
  </div>
</template>

<script>
export default {
  name: "PizzaCard",
  props: {
    name: String,
    description: String,
    price: Number,
  },
};
</script>
