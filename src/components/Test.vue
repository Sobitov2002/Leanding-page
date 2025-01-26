<script setup lang="ts">
import { ref } from 'vue';
import Dialog from './Dialog.vue';

const footer = ref<HTMLElement | null>(null);
</script>

<template>
    <div class="prise-img min-h-screen w-full pt-10 z-10">
        <div class="container px-1">
            <div class="grid md:grid-cols-2 grid-cols-1 gap-4">
                <div class="md:mt-[110px] w-[90%] m-auto ">
                    <div class="w-[171.68px] md:w-[362px] m-auto bg-white rounded-[7.52px] ">
                        <div
                            class="text-[#CB7C7E] text-start font-[gilroy] p-[7px] md:p-5 leading-[24.3px]  text-[19.63px] md:text-[40.39px] drop-shadow-lg   ">
                            1,2,3 fevral 20:00
                        </div>
                    </div>
                    <div class="mt-[16px] lg:mt-[28px] relative">
                        <h1
                            class="font-[gilroy] md:text-start drop-shadow-[0_1.73px_1.73px_#000000] leading-[30.7px] md:leading-[60.05px] text-white lg:text-[.43px] md:text-[50px] ld:text-[60px] text-center text-[32.88px]">
                            0 dan 3 oyda TOPIK 2
                            qadam ma qadam
                        </h1>
                        <p
                            class="drop-shadow-[0_1.73px_1.73px_#000000] md:text-start md:mt-[40px] w-[90%] m-auto text-[16.67px] lg:text-[42.73px] md:text-[40px] md:leading-[42.9px] leading-[24.35px] text-white font-[gilroy] text-center">
                            Master klassga qatnashish uchun xavoladan o‘ting
                        </p>
                        <span
                            class="text-[50.22px]  drop-shadow-[0_3.89px_3.89px]  lg:text-[86.04px] md:text-[50px]  md:leading-[101.34px] absolute md:right-20 right-5 md:-bottom-16 text-[#A43D3F] leading-[40.22px] font-[Freestyle]">Master
                            klass
                        </span>
                    </div>
                    <div
                        class=" items-center md:block hidden  justify-center w-full md:left-0 mb-2 md:mt-[121px] md:w-auto md:mx-0">
                        <div class="w-full md:w-auto">
                            <Dialog />
                        </div>
                    </div>
                    <div
                        class="flex md:hidden items-center justify-center  md:w-full md:left-0 mt-10 md:mt-[121px]  absolute bottom-5 left-1/2 transform -translate-x-1/2 z-20 md:mx-0">
                        <div class="w-[351.66px] flex justify-center md:w-auto">
                            <Dialog />
                        </div>
                    </div>


                </div>
                <div class="w-[90%] ">
                    <div
                        class="absolute md:relative lg:-bottom-[110px] md:-bottom-[210px] bottom-0 z-10 w-full left-1/2 transform -translate-x-1/2 md:right-auto right-0">
                        <div class="relative flex justify-center">
                            <img class="w-auto md:h-[692px] h-[355.53px] lg:h-[790px]"
                                src="../assets/image/Layer 12 1.png" alt="Banner Img">
                        </div>

                        <!-- Matnni pastga joylashtirish -->
                        <div class="absolute md:bottom-16 bottom-[50px] w-[80%] m-auto md:w-full ">
                            <p
                                class="text-[40.16px] md:text-[60px] w-[80%] m-auto text-[#fff] leading-[25.22px] font-[Freestyle]">
                                Topik yuqori ball olish va Koreya
                            </p>
                            <h1
                                class="lg:text-[80.27px] mb-7 md:text-[60px] leading-[40px] w-[80%] m-auto text-[40.88px] text-white font-[oswald] font-bold md:leading-[100.78px]">
                                MADINA QODIROVA
                            </h1>
                        </div>

                        <div style="opacity: 0.2;" class="absolute bottom-[220px] text-center lg:left-[200px] md:left-[10px] inset-0 flex items-center justify-center 
         drop-shadow-[0_8.73px_8.73px_#000000] text-opacity-70 
         lg:text-[10px] xl:text-[180px] md:text-[70px] md:leading-[70px] lg:leading-[120px] xl:leading-[150px] text-[77.91px] font-[oswald] 
         leading-[100px] font-bold -z-20 text-white">
                            MADINA QODIROVA
                        </div>
                    </div>

                </div>



            </div>
        </div>
    </div>
</template>

<style scoped>
.myfont {
    text-shadow: 0 0.89px 0.89px 0;
}

.text-shadow {
    text-shadow: 0 0.89px 0.89px 0;
}
</style>
