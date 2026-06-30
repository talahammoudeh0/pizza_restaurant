<template>
    <nav class=" bg-black text-white px-6 py-4 flex justify-between items-center flex-wrap">
        <h2 class="text-red-400 text-xl font-bold">Pizza Home</h2>
        <div class="flex gap-6">
            <button @click="currentPage = 'Home'" class="cursor-pointer hover:text-red-400">Home</button>
            <button @click="currentPage = 'About'" class="cursor-pointer hover:text-red-400">About</button>
        </div>
    </nav>

    <component :is="currentPage" @goBack="currentPage = 'Home'" />
</template>

<script>
import { ref } from 'vue'
import Home from './views/HomeView.vue'
import About from './views/AboutView.vue'

export default {
    name: 'App',
    components: { Home, About },
    setup() {
        const currentPage = ref('Home')

        return { currentPage }
    }
}
</script>