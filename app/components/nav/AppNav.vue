<template>
    <header class="fixed  top-0 left-0 py-2 sm:py-3 md:py-6 px-4 w-full self-container z-50 bg-black">
        <nav class="flex-between w-full">
            <NuxtLink to="/"
                class="p-1 cursor-pointer transfor hover:-translate-y-0.5 transition-transform duration-200">
                <img class="h-10 " src="/logo.svg" alt="logo">
            </NuxtLink>
            <div class="md:flex-center gap-1 hidden">
                <NuxtLink class="p-2 hover:text-white transition-colors duration-200" v-for="(item, idx) in navigation"
                    :class="route.path === item.path ? 'text-white' : ''
                        " :key="idx" :to="item.path">{{ item.name }}</NuxtLink>
            </div>
            <div class="flex-center">
                <div class="p-0.5 cursor-pointer transfor hover:-translate-y-0.5 transition-transform duration-200">
                    <img class="h-8 " src="/search.svg" alt="Search">
                </div>
                <div class="p-0.5 cursor-pointer transfor hover:-translate-y-0.5 transition-transform duration-200">
                    <img class="h-8 " src="/cart.svg" alt="Cart">
                </div>
            </div>
        </nav>
    </header>
</template>

<script lang="ts" setup>
const route = useRoute()
const navigation = ref([
    {
        name: "Home",
        path: '/'
    },
    {
        name: "Mac",
        path: '/mac'
    },
    {
        name: "Chip",
        path: '/chip'
    },
    {
        name: "Graphics",
        path: '/graphics'
    },
    {
        name: "Features",
        path: '/features'
    },
    {
        name: "Follow",
        path: '/follow'
    },
])
</script>
