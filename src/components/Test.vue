<script setup lang="ts">
import { ref } from 'vue';
import Dialog from './Dialog.vue'
// import Price from '@/components/price/Price.vue'

const footer = ref<HTMLElement | null>(null);


</script>

<template>
    <div class="prise-img md:h-screen h-[700px] w-full py-10 z-10 relative">
        <div class="absolute bottom-0  left-0 w-full h-full z-[-1]">
            <img class=" md:block sm:h-[600px] h-[692px] pt-20 sm:p-0 md:h-[692px] bottom-0 lg:h-[790px] w-auto mx-auto absolute md:left-1/2    transform -translate-x-1/2"
                src="https://ik.imagekit.io/vtroph5l9/Product/s.png?updatedAt=1737760939112" alt="Banner Img">
        </div>
        <div class="">
            <!-- First section -->

            <!-- Next section -->
            <div class="">
                <div class="grid md:grid-cols-2 w-[90%]  sm:container m-auto grid-cols-1 relative  top-14 ">
                    <h1
                        class="text-white font-[Freestyle] lg:text-[55px] md:text-[50px] text-[39px] md:block  md:text-start text-end ">
                        Topik
                        yuqori ball olish va Koreya </h1>

                    <h1 class="text-white  font-[Freestyle] text-[55px] md:text-[50px] md:block hidden text-end ">
                        Topik
                        yuqori ball
                        olish
                        va Koreya</h1>
                </div>
                <div class="md:container w-[90%] m-auto  mt-5">

                    <!-- Next section -->
                    <div class="md:flex  md:justify-between p-0 justify-end ">
                        <h1 class="text-[#A43D3F]  font-[oswald] text-[60px]  font-bold  md:text-[90.27px] text-end  ">
                            MADINA</h1>
                        <div></div>
                        <h1
                            class="text-[#A43D3F] hidden md:block  font-[oswald] text-[60px]  font-bold  md:text-[90.27px] text-end">
                            MADINA</h1>
                    </div>
                    <!-- Next section -->

                    <div class="flex relative md:justify-between  justify-end bottom-10">
                        <h1 class="text-[#A43D3F]  font-[oswald] font-bold md:text-[90.27px] text-end  text-[60px]">
                            QODIROVA</h1>
                        <div></div>
                        <h1
                            class="text-[#A43D3F]  top-10 font-[oswald] font-bold lg:text-[90.27px] text-end hidden md:block text-[75px]">
                            QODIROVA</h1>
                    </div>

                    git push -u origin main
                </div>
            </div>
        </div>

        <!-- Next section -->
        <div class="flex md:justify-center justify-end">

            <div class=" sm:w-auto">
                <p
                    class="text-[#de878a] block   rounded-[20.14px] px-5 py-1 bg-white md:text-[18.53px] lg:text-[45px] sm:text-[20px] text-[22px] cursor-pointer font-[gilroy] shadow-lg text-shadow">
                    1,2,3 fevral
                </p>
            </div>

        </div>
        <div class="flex  md:justify-center justify-end">
            <h1 class="font-[gilroy] text-white md:text-[55px] text-end text-[35px] ">
                Bepul Master klassgataklif qilaman
            </h1>
        </div>
        <div class="flex justify-center">
            <Dialog />
        </div>


    </div>

</template>

<style scoped>

 
</style>
