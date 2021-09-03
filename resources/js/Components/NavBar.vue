<template>
    <div class="antialiased min-h-screen relative lg:flex">
        <nav class="absolute inset-0 transform lg:transform-none lg:opacity-100 duration-200 -translate-x-full lg:relative z-10 w-48 bg-yellow-500 text-white h-screen p-3" :class="{'open' :showNavBar}" @close="showNavBar = false">
            <div class="flex justify-between">
                <span class="font-bold text-2xl sm:text-3xl p-2">Sidebar</span>
                <button class="p-2 focus:outline-none focus:bg-yellow-400 hover:bg-yellow-400 rounded-md lg:hidden" @click="toggleNavBar()">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                    </svg>
                </button>
            </div>
            <NavBarLink>hello</NavBarLink>
            <NavBarLink>hi</NavBarLink>
        </nav>
        <div class="relative z-0 lg:flex-grow">
            <header class="flex bg-red-700 text-white items-center">
                <button class="p-2 focus:outline-none focus:bg-red-400 hover:bg-red-400 rounded-md" @click="toggleNavBar()">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
                    </svg>
                </button>
                <span class="block text-2xl sm:text-3xl font-bold text-white p-4">Joe's Crab Shack</span>
            </header>
        </div>
    </div>
</template>
<script>
import NavBarLink from '@/Components/NavBarLink';

export default {
    data() {
        return {
            showNavBar: false,
        }
    },

    methods: {
        toggleNavBar() {
            this.showNavBar = !this.showNavBar;
        }
    },

    components: {
            NavBarLink,
    },
}
</script>
