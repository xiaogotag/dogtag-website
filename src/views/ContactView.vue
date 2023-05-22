<template>
    <div class="container mx-auto px-4 py-8">
        <div class="text-center">
            <h1 class="text-4xl font-bold text-gray-800 mb-4">Contactez-nous</h1>
            <p class="text-gray-600 mb-8">N'hésitez pas à nous contacter pour toute question ou demande d'information.</p>
        </div>

        <div class="max-w-lg mx-auto">
            <form @submit.prevent="submitForm" class="space-y-4">
                <div>
                    <label for="name" class="block text-gray-800 font-semibold mb-1">Nom complet</label>
                    <input v-model="formData.name" type="text" id="name" class="w-full border border-gray-300 rounded py-2 px-4" />
                </div>

                <div>
                    <label for="email" class="block text-gray-800 font-semibold mb-1">Adresse e-mail</label>
                    <input v-model="formData.email" type="email" id="email" class="w-full border border-gray-300 rounded py-2 px-4" />
                </div>

                <div>
                    <label for="message" class="block text-gray-800 font-semibold mb-1">Message</label>
                    <textarea v-model="formData.message" id="message" class="w-full border border-gray-300 rounded py-2 px-4" rows="5"></textarea>
                </div>

                <button type="submit" class="bg-blue-500 text-white py-2 px-4 rounded font-semibold hover:bg-blue-600">Envoyer</button>
            </form>
        </div>
    </div>
</template>

<script setup>
import { ref } from "vue";

const formData = ref({
    name: "",
    email: "",
    message: ""
});
</script>
