<template>
<header class="flex justify-between items-center px-8 bg-gray-800 h-16 w-full text-gray-400 relative sm:h-24" :class="{'shadow-md': !navActive}">
    
    <!-- Mobile Nav Toggle and Close Btn -->
    <div class="sm:hidden">
        <i class="fas fa-bars text-xl hover:text-gray-200 cursor-pointer" @click="toggleNav" v-if="!navActive"></i>
        <i class="fas fa-times text-xl text-gray-200 hover:text-gray-50 cursor-pointer" @click="toggleNav" v-else></i>
    </div>

    <!-- Nav Mobile Menu -->
    <nav class="h-96 w-full bg-gray-800 shadow-2xl p-4 text-gray-400 text-xl flex flex-col justify-around absolute left-0 top-16 sm:hidden z-40" v-if="navActive">
        <a href="/" class="mx-2 px-4 py-2 hover:bg-gray-900 border-l-4 transform transition-all ease-in-out duration-300 hover:text-gray-200 hover:translate-x-4">Home</a>
        <a href="/" class="mx-2 px-4 py-2 hover:bg-gray-900 transform transition-all ease-in-out duration-300 hover:text-gray-200 hover:translate-x-4">Services</a>
        <a href="/" class="mx-2 px-4 py-2 hover:bg-gray-900 transform transition-all ease-in-out duration-300 hover:text-gray-200 hover:translate-x-4">Blog</a>
        <div class="mx-2 px-4 py-2 w-12/12 hover:bg-gray-900 transform transition-all ease-in-out duration-300 hover:text-gray-200 hover:translate-x-4 flex justify-between items-center cursor-pointer">
            <span>Projects</span>
            <i class="fas fa-caret-down transform" :class="dropDownMenu? 'rotate-0' : '-rotate-90'" @click="toggleDropdown"></i>
        </div>
        
        <!-- Mobile DropDown -->
        <ul class="w-48 bg-gray-50 text-gray-400 flex flex-col absolute right-0 -bottom-52 shadow-2xl" v-if="dropDownMenu">
            <a href="#" class="flex justify-center items-center py-4 hover:bg-gray-700">
                <li>Movie App</li>
            </a>
            <a href="#" class="flex justify-center items-center py-4 hover:bg-gray-700">
                <li>Marketing Site</li>
            </a>
            <a href="#" class="flex justify-center items-center py-4 hover:bg-gray-700">
                <li>Weather App</li>
            </a>
            <a href="#" class="flex justify-center items-center py-4 hover:bg-gray-700">
                <li>Project 4</li>
            </a>
        </ul>
    </nav>

      <!-- Logo -->
    <!-- <div class="bg-gray-50 border-gray-700 border rounded">
        <img src="../assets/danncodes.png" alt="" class="h-11">
    </div> -->

    <!-- Desktop Nav -->
    <nav class="hidden w-6/12 lg:w-5/12 xl:w-4/12 h-full ml-4 text-gray-400 text-md md:text-lg sm:flex justify-around items-center" @mouseleave="dropDownMenu = false">
        <a href="/" class="px-4 py-4 hover:bg-gray-900 transform transition-all ease-in-out duration-300 hover:text-gray-200 hover:-translate-y-4">Home</a>
        <a href="/" class="px-4 py-4 hover:bg-gray-900 transform transition-all ease-in-out duration-300 hover:text-gray-200 hover:-translate-y-4">Services</a>
        <a href="/" class="px-4 py-4 hover:bg-gray-900 transform transition-all ease-in-out duration-300 hover:text-gray-200 hover:-translate-y-4">Blog</a>
        <a href="/" class="px-4 py-4 hover:bg-gray-900 transform transition-all ease-in-out duration-300 hover:text-gray-200 hover:-translate-y-4 flex justify-between items-center" @mouseenter="dropDownMenu = true" @mouseleave="dropDownMenu = false">
         <!-- Desktop DropDown -->
        <span class="relative">Projects
        <ul class="w-48 bg-gray-50 text-gray-400 flex flex-col absolute -bottom-54 left-8 shadow-2xl" v-if="dropDownMenu" @mouseenter="dropDownMenu = true" @mouseleave="dropDownMenu = false">
            <a href="#" class="flex justify-center items-center py-4 hover:bg-gray-700">
                <li>Movie App</li>
            </a>
            <a href="#" class="flex justify-center items-center py-4 hover:bg-gray-700">
                <li>Marketing Site</li>
            </a>
            <a href="#" class="flex justify-center items-center py-4 hover:bg-gray-700">
                <li>Weather App</li>
            </a>
            <a href="#" class="flex justify-center items-center py-4 hover:bg-gray-700">
                <li>Project 4</li>
            </a>
        </ul>
        </span>
        <i class="fas fa-caret-down transform pointer-events-none ml-1" :class="dropDownMenu? 'rotate-0' : '-rotate-90'" @mouseover="dropDownMenu = true"></i>
    </a>
    
    
    </nav>

    <!-- Nav Social Media Links -->
    <div>
        <a href="https://www.linkedin.com/in/daniel-mensah-156270136/" target="_blank">
            <i class="fab fa-linkedin-in px-1 hover:text-gray-200 cursor-pointer"></i>
        </a>
        <a href="https://github.com/danncodes" target="_blank">
            <i class="fab fa-github px-1 hover:text-gray-200 cursor-pointer"></i>
        </a>
        <a href="#" target="_blank">
            <i class="fab fa-instagram px-1 hover:text-gray-200 cursor-pointer"></i>
        </a>
        <a href="https://twitter.com/danncodes" target="_blank">
            <i class="fab fa-twitter px-1 hover:text-gray-200 cursor-pointer"></i>
        </a>
    </div>
</header>
  
</template>
<script>
import Button from "./Button.vue"
export default {
    components: {Button},
    data(){
        return {
            navActive: false,
            dropDownMenu: false
        }
    },
    methods: {
        toggleNav(){
            this.navActive = !this.navActive
        },
        toggleDropdown(){
            this.dropDownMenu = !this.dropDownMenu
        }
        
    }

}
</script>