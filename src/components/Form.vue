<template>
    <form @submit.prevent="submit" class="mt-0 mx-auto  bg-white rounded  w-[100%]" v-if="!isSuccess">
        <h1 class="text-[#A43D3F] text-[25px] py-1 font-[oswald] text-center w-[100%]">
            Joyingizni band qilish uchun ma'lumotlaringizni yuboring!
        </h1>
        <div>
            <label class="block mt-2" for="firstName">Ismingizni kiriting</label>
            <input required v-model="formData.firstName" id="firstName" type="text"
                class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                placeholder="Ism" :disabled="isLoading" />
        </div>
        <div>
            <label class="block mt-2" for="lastName">Familyangizni kiriting</label>
            <input required v-model="formData.lastName" id="lastName" type="text"
                class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                placeholder="Familya" :disabled="isLoading" />
        </div>
        <div class="mt-3">
            <label class="block text-gray-700 mt-2" for="phoneNumber">Telefon raqamingiz</label>
            <input required v-model="formData.phoneNumber" id="phoneNumber" type="number"
                class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
                placeholder="+998" :disabled="isLoading" />
        </div>
        <div class="mt-4">
            <Button :isLoading="isLoading" :disabled="isLoading">Saqlash</Button>
        </div>
    </form>

    <!-- Telegram kanaliga o'tish tugmasi faqat isSuccess bo'lganda ko'rinadi -->
    <div v-if="isSuccess" class="mt-4 text-center">
        <a href="https://t.me/+uKeFjV3ft_dlYzky" target="_blank"
            class="inline-block bg-green-500 text-white py-2 text-[20px] px-4 rounded-lg">
            Telegram kanaliga o'tmoqda...
        </a>
    </div>
</template>

<script setup lang="ts">
import { ref, defineEmits } from 'vue';
import axios from 'axios';
import Button from './ui/Button.vue';

const emit = defineEmits(['updateDialogOpen']);

const formData = ref({
    lastName: '',
    firstName: '',
    phoneNumber: '',
});

const isSuccess = ref(false);
const dialogOpen = ref(false);
const isLoading = ref(false);

const submit = async () => {
    isLoading.value = true;

    const currentDate = new Date();
    const formattedDate = currentDate.toLocaleDateString('en-GB');
    const formattedTime = currentDate.toLocaleTimeString('en-GB', { hour12: false });

    const text = `🆕 Yangi foydalanuvchi:
👤 Ism: ${formData.value.firstName} ${formData.value.lastName}
📞 Telefon: ${formData.value.phoneNumber}
📅 Sana: ${formattedDate}
🕒 Vaqt: ${formattedTime}`;

    try {
        const token = '7749260469:AAEgInZHdGNda-9FviCu_8E9C7fSrgmQKnc';
        const chatId = '5812196124';

        // Telegramga yuborish
        await axios.post(`https://api.telegram.org/bot${token}/sendMessage?chat_id=${chatId}&text=${encodeURIComponent(text)}`);

        // Yuborish muvaffaqiyatli bo'lsa
        isSuccess.value = true;
        dialogOpen.value = false;
        emit('updateDialogOpen', dialogOpen.value);

        formData.value = { firstName: '', lastName: '', phoneNumber: '' };

        // Telegram kanaliga yo'naltirish
        setTimeout(() => {
            window.location.href = 'https://t.me/+uKeFjV3ft_dlYzky'; // Telegram kanaliga o'tish
        }, 1000); // 2 soniyadan keyin o'tish
    } catch (error) {
        console.error('Xatolik:', error);
        isSuccess.value = false;
        alert("Xatolik yuz berdi. Iltimos, qayta urinib ko'ring.");
    } finally {
        isLoading.value = false;
    }
};
</script>

