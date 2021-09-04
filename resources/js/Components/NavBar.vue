<template>
    <div class="antialiased min-h-screen relative lg:flex">
        <!----------NAVBAR---------->
        <nav v-if="showNavBar" class="absolute inset-0 transform lg:transform-none lg:opacity-100 duration-200 -translate-x-full lg:relative z-10 w-48 bg-yellow-500 text-white h-screen p-3">
            <div class="flex justify-between">
                <span class="font-bold text-2xl sm:text-3xl p-2">Sidebar</span>
            </div>
            <NavBarLink>hello</NavBarLink>
            <NavBarLink>hi</NavBarLink>
        </nav>

        <div class="relative z-0 lg:flex-grow">
            <header class="flex bg-red-700 text-white items-center">
                <button class="p-2 focus:outline-none focus:bg-red-400 hover:bg-red-400 rounded-md" v-on:click="showNavBar = !showNavBar">
                    <div v-if="showNavBar">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
                        </svg>
                    </div>
                    <div v-if="!showNavBar">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                        </svg>
                    </div>
                </button>
                <span class="block text-2xl sm:text-3xl font-bold text-white p-4">Joe's Crab Shack</span>
                <!-- <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1" />
                </svg> -->
            </header>
            
            <div>
                this is the main part
            </div>
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
