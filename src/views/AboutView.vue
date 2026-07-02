<template>
  <div class="min-h-screen bg-gray-400 text-white">
    <div 
      class="w-full h-40 bg-cover bg-center flex items-center justify-center"
      style="background-image: url('https://images.presentationgo.com/2025/04/pepperoni-pizza-closeup.jpg')"
    >
      <h1 class="text-white text-4xl font-bold bg-black/80 px-6 py-3 rounded-lg">
        About Us
      </h1>
    </div>

    <div class="px-6 py-10">
      <p
        class="text-center text-black font-bold max-w-xl mx-auto mb-8 text-sm md:text-base font-Poppins"
      >
        Pizza Home was founded in 2010. We serve the finest authentic Italian
        pizza made with fresh ingredients daily.
      </p>

      <h2 class="text-center text-red-700 text-2xl font-bold mb-8 font-serif">Our Menu</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-4xl mx-auto">
        <PizzaCard
          v-for="pizza in pizzas"
          :key="pizza.id"
          :name="pizza.name"
          :description="pizza.description"
          :price="pizza.price"
          :image="pizza.image"
        />
      </div>

      <div class="flex justify-center pt-10">
        <button
          @click="goBack"
          class="border border-red-500 bg-red-100 text-black px-4 py-2 rounded-lg cursor-pointer hover:bg-red-300"
        >
          Back
        </button>
      </div>

    </div>

  </div>
</template>

<script>
import PizzaCard from "../components/PizzaCard.vue";

export default {
  name: "About",
  components: { PizzaCard },
  emits: ["goBack"],
  setup(props, { emit }) {
    const pizzas = [
      {
        id: 1,
        name: "Margherita",
        description: "Tomato sauce, mozzarella, basil",
        price: 5,
        image:"public/Pizza Margherita.webp"
      },
      {
        id: 2,
        name: "Pepperoni",
        description: "Tomato sauce, mozzarella, pepperoni",
        price: 6,
        image:"public/Pizza pepperoni.jpg"
      },
      {
        id: 3,
        name: "Alfredo",
        description: "Alfredo sauce, mozzarella, mushroom",
        price: 6,
        image:"public/Pizza Alfredo.jpg"
      },
    ];

    const goBack = () => {
      emit("goBack");
    };

    return { pizzas, goBack };
  },
};
</script>