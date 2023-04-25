<template>
    <div>
        <div class="bg-orange-100">
            <nav class="container px-6 py-3 mx-auto md:flex md:justify-between md:items-center">
                <div class="flex items-center justify-between sm:flex sm:items-center">
                    <div class="flex">
                        <router-link to="/" class="text-xl text-amber-900 md:text-2xl hover:text-blue-400"><img src="@/assets/logo_notext.png" class="object-contain h-6" /> </router-link>
                    </div>
                    <!-- Mobile menu button -->
                    <div @click="showMenu = !showMenu" class="flex md:hidden">
                        <button type="button" class="text-amber-900 hover:text-gray-400 focus:outline-none focus:text-gray-400">
                            <font-awesome-icon icon="fa-solid fa-bars" />
                        </button>
                    </div>
                </div>

                <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
                <ul :class="showMenu ? 'flex' : 'hidden'" class="flex-col mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0">
                    <li class="text-sm text-amber-900 hover:text-blue-400">Home</li>
                    <li class="text-sm text-amber-900 hover:text-blue-400">About</li>
                    <li class="text-sm text-amber-900 hover:text-blue-400">Blogs</li>
                    <li class="text-sm text-amber-900 hover:text-blue-400">Contact Us</li>
                </ul>
            </nav>
        </div>
    </div>
    <RouterView />
</template>

<script setup>
import { library } from "@fortawesome/fontawesome-svg-core";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faBars } from "@fortawesome/free-solid-svg-icons";

import { RouterLink, RouterView } from "vue-router";
import { ref } from "vue";

library.add(faBars);

const showMenu = ref(false);
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto+Condensed");

* {
    font-family: "Roboto Condensed", sans-serif;
}
</style>
