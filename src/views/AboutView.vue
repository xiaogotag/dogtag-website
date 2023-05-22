<template>
    <header class="bg-white pt-4">
        <div class="container mx-auto px-4 py-4 text-center">
            <h1 class="text-gray-800 text-4xl font-bold mb-4">Notre Équipe</h1>
            <p class="text-gray-600 text-lg">Découvrez les membres talentueux qui composent notre équipe.</p>
        </div>
    </header>

    <div class="flex flex-wrap m-4">
        <div v-for="member in members" class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/4 px-4 mb-8">
            <div class="bg-white shadow-lg rounded-lg overflow-hidden">
                <img :src="member.photo" :alt="'Photo de ' + member.name" class="w-full h-48 object-cover object-center" />
                <div class="p-4">
                    <h3 class="text-xl font-medium text-gray-800">{{ member.name }}</h3>
                    <p class="text-gray-600 mb-4">{{ member.role }}</p>
                    <ul class="flex flex-wrap gap-1">
                        <li v-for="skill in member.skills" class="bg-gray-200 text-gray-700 px-2 py-1 rounded">
                            {{ skill }}
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from "vue";

const members = ref([
    {
        name: "Julien Augugliaro",
        photo: "https://i.imgur.com/vblzFeG.jpg",
        role: "Développeur backend",
        skills: ["Node.js", "Docker", "NoSQL", "Firebase"]
    },
    {
        name: "Marius Contoli",
        photo: "https://i.imgur.com/zz2NnwX.jpg",
        role: "Développeur frontend",
        skills: ["Angular"]
    },
    {
        name: "Eloise Richard",
        photo: "https://i.imgur.com/1B7L4k4.jpg",
        role: "Développeur backend",
        skills: ["Node.js", "Docker", "NoSQL", "Firebase"]
    },
    {
        name: "Youssra El Ajli",
        photo: "https://i.imgur.com/tGkIhBW.jpg",
        role: "Développeur backend",
        skills: ["Node.js", "Docker", "NoSQL", "Firebase"]
    },
    {
        name: "Jeremy Dumesny",
        photo: "https://i.imgur.com/jxD9JSo.jpg",
        role: "Développeur mobile",
        skills: ["Flutter", "iOS", "Android"]
    },
    {
        name: "Hugo Suzanne",
        photo: "https://i.imgur.com/9D4AyWK.jpg",
        role: "Développeur mobile",
        skills: ["Flutter", "iOS", "Android"]
    },
    {
        name: "Konstantin Kurilov",
        photo: "https://i.imgur.com/xh2zLVH.jpg",
        role: "Développeur hardware",
        skills: ["Arduino", "C++"]
    },
    {
        name: "Alizee Patricola",
        photo: "https://i.imgur.com/e3cMJpp.jpg",
        role: "Développeur hardware",
        skills: ["Arduino"]
    }
]);
</script>
