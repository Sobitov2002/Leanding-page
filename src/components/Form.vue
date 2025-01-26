<template>
    <form @submit.prevent="submit" class="mt-0 mx-auto bg-white rounded w-full" v-if="!isSuccess">
        <h1 class="text-[#A43D3F] text-[25px] py-1 font-[oswald] text-center w-full">
            Joyingizni band qilish uchun ma'lumotlaringizni yuboring!
        </h1>

        <!-- First Name Input -->
        <div>
            <label class="block text-left mt-2" for="firstName">Ism familya kiriting</label>
            <input required v-model="formData.firstName" id="firstName" type="text"
                class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                placeholder="Ism familya " :disabled="isLoading" />
        </div>

        <!-- Phone Number Input with Country Code -->
        <div class="mt-3">
            <label class="block text-left text-gray-700 mt-2" for="phoneNumber">Telefon raqamingiz</label>
            <input required v-model="formData.phoneNumber" id="phoneNumber" type="tel"
                class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                placeholder="+998" :disabled="isLoading" value="+998" />
        </div>

        <!-- Submit Button -->
        <div class="mt-4">
            <Button :isLoading="isLoading" :disabled="isLoading">Saqlash</Button>
        </div>
    </form>

    <!-- Success Message with Telegram Link -->
    <div v-if="isSuccess" class="mt-4 text-center">
        <a href="https://t.me/+uKeFjV3ft_dlYzky" target="_blank"
            class="inline-block bg-green-500 text-white py-2 text-[20px] px-4 rounded-lg">
            Telegram kanaliga o'tmoqda...
        </a>
    </div>
</template>

<script setup lang="ts">
import { ref, onMounted, defineEmits } from 'vue';
import axios from 'axios';
import Button from './ui/Button.vue';

const emit = defineEmits(['updateDialogOpen']);

const formData = ref({
    firstName: '',
    phoneNumber: '+998',  // Default value for phone number
});

const isSuccess = ref(false);
const isLoading = ref(false);

onMounted(() => {
    // Optional: Add phone number input formatting or validation here
});

const submit = async () => {
    isLoading.value = true;

    const currentDate = new Date();
    const formattedDate = currentDate.toLocaleDateString('en-GB');
    const formattedTime = currentDate.toLocaleTimeString('en-GB', { hour12: false });

    const text = `🆕 Yangi foydalanuvchi:
👤 Ism Familya: ${formData.value.firstName}
📞 Telefon: ${formData.value.phoneNumber}
📅 Sana: ${formattedDate}
🕒 Vaqt: ${formattedTime}`;

    try {
        const token = '7749260469:AAEgInZHdGNda-9FviCu_8E9C7fSrgmQKnc';
        const chatId = '-1002370103265';

        // Send message to Telegram
        await axios.post(`https://api.telegram.org/bot${token}/sendMessage?chat_id=${chatId}&text=${encodeURIComponent(text)}`);

        // On success
        isSuccess.value = true;
        formData.value = { firstName: '', phoneNumber: '+998' };

        // Redirect to Telegram channel after a short delay
        setTimeout(() => {
            window.location.href = 'https://t.me/+uKeFjV3ft_dlYzky'; // Redirect to Telegram channel
        }, 1000); // 1 second delay
    } catch (error) {
        console.error('Xatolik:', error);
        isSuccess.value = false;
        alert("Xatolik yuz berdi. Iltimos, qayta urinib ko'ring.");
    } finally {
        isLoading.value = false;
    }
};
</script>
