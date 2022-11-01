<script>

export default {
    data(){
        return{
            isOpen: false
        }
    },

    methods: {
        toggle(){
            this.isOpen = ! this.isOpen
        }
    }
}

</script>

<template>

    <nav class="relative w-full">
        <div class="container py-4 mx-auto w-full">
            <div class="lg:flex lg:items-center lg:justify-between w-full">
                
                <div class="flex items-center justify-between">

                    <div class="text-xl font-semibold text-gray-700">
                        <a class="text-xl font-semibold text-gray-800 transition-colors duration-300 transform dark:text-white lg:text-3xl hover:text-gray-700 dark:hover:text-gray-300" href="#">
                            Dark Weather
                        </a>
                    </div>

                    <div class="flex lg:hidden">
                        <button  v-on:click="toggle"  type="button" class="text-gray-500 dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none focus:text-gray-600 dark:focus:text-gray-400" aria-label="toggle menu">
                            <svg v-show="!isOpen" mlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M4 8h16M4 16h16" />
                            </svg>
                    
                            <svg v-show="isOpen" xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                            </svg>
                        </button>
                    </div>
                </div>

                <div :class="[isOpen ? 'translate-x-0 opacity-100 ' : 'opacity-0 translate-x-full']" class="absolute inset-x-0 z-20 w-full px-6 py-4 transition-all duration-300 ease-in-out bg-white dark:bg-gray-800 lg:mt-0 lg:p-0 lg:top-0 lg:relative lg:bg-transparent lg:w-auto lg:opacity-100 lg:translate-x-0 lg:flex lg:items-center lg:justify-between">
                    <div class="flex  flex-col -mx-6 lg:flex-row lg:items-center lg:mx-8">
                        <a href="#" class="px-3 py-2 mx-3 mt-2 text-gray-700 transition-colors duration-300 transform rounded-md lg:mt-0 dark:text-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">Home</a>
                        <a href="#" class="px-3 py-2 mx-3 mt-2 text-gray-700 transition-colors duration-300 transform rounded-md lg:mt-0 dark:text-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">Download App</a>
                        <a href="#" class="px-3 py-2 mx-3 mt-2 text-gray-700 transition-colors duration-300 transform rounded-md lg:mt-0 dark:text-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">Contact Us</a>
                    </div>

                    <div class="flex items-center mt-4 lg:mt-0">
                        <button class="py-3 px-8 rounded-lg bg-gradient-to-t from-[#3A5E72] to-[#3A5E72] text-white">
                            Sign Up
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </nav>

</template>
