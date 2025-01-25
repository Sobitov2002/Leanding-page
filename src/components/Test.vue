<script setup lang="ts">
import { ref } from 'vue';
import Dialog from './Dialog.vue'
// import Price from '@/components/price/Price.vue'

const footer = ref<HTMLElement | null>(null);


</script>

<template>
    <div class="prise-img min-h-screen  w-full py-10 z-10 relative">
        <div class="absolute bottom-0 left-0 w-full h-full z-[-1]">
            <img class="w-auto  sm:h-[800px] md:h-[692px] h-[50%] lg:h-[790px] mx-auto absolute bottom-0 left-1/2 transform -translate-x-1/2"
                src="https://ik.imagekit.io/vtroph5l9/Product/s.png?updatedAt=1737760939112" alt="Banner Img">
        </div>

        <div class="">
            <!-- First section -->

            <!-- Next section -->
            <div class="">
                <div class="grid md:grid-cols-2 w-[90%]  sm:container m-auto grid-cols-1 relative  md:top-14 top-0 ">
                    <h1
                        class="text-white font-[Freestyle] lg:text-[55px] md:text-[50px] text-[60px] md:block md:text-start text-center tracking-wide leading-10">
                        0 dan 2 oyda TOPIK 2 qadam va qadam
                    </h1>
                    <h1 class="text-white  font-[Freestyle] text-[60px] md:text-[55px] md:block hidden text-end ">
                        0 dan 2 oyda TOPIK 2 qadam va qadam </h1>
                </div>
                <div class="md:container w-[90%] m-auto ">

                    <!-- Next section -->
                    <div class="md:flex  md:justify-between p-0 justify-end -bottom-15 ">
                        <h1
                            class="text-[#A43D3F]  font-[oswald] text-[30px]  font-bold   md:text-[90.27px] text-center  ">
                            MADINA</h1>
                        <div></div>
                        <h1
                            class="text-[#A43D3F] hidden md:block  font-[oswald] text-[60px]  font-bold  md:text-[90.27px] text-end">
                            MADINA</h1>
                    </div>
                    <!-- Next section -->

                    <div class="flex relative md:justify-between  justify-center md:bottom-10 bottom-5  ">
                        <h1 class="text-[#A43D3F] font-[oswald] font-bold md:text-[90.27px] text-[32px] text-center">
                            QODIROVA
                        </h1>

                        <div></div>
                        <h1
                            class="text-[#A43D3F]  top-10 font-[oswald] font-bold lg:text-[90.27px] text-end hidden md:block text-[75px]">
                            QODIROVA</h1>
                    </div>


                </div>
            </div>
        </div>

        <!-- Next section -->
        <div class="flex justify-center md:mt-20 -mt-6">

            <div class=" sm:w-auto">
                <p
                    class="text-[#de878a] block   rounded-[20.14px] px-5 py-1 bg-white md:text-[18.53px] lg:text-[45px] sm:text-[20px] text-[22px] cursor-pointer font-[gilroy] shadow-lg text-shadow">
                    1,2,3 fevral 21:00
                </p>
            </div>

        </div>
        <div class="flex   justify-center">
            <h1 class="font-[gilroy] text-white md:text-[55px] text-center text-[28px] ">
                Bepul Master-klassga taklif qilaman
            </h1>
        </div>
        <div class="flex justify-center items-center absolute  left-1/2 bottom-5 transform -translate-x-1/2  w-full">
            <Dialog />
        </div>



    </div>

</template>

<style scoped>

 
</style>
