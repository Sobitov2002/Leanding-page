<script setup lang="ts">
import {
    Dialog,
    DialogContent,
    DialogDescription,
    DialogFooter,
    DialogHeader,
    DialogTitle,
    DialogTrigger,
} from '@/components/ui/dialog'
import Form from './Form.vue'
</script>

<template>
    <Dialog>
        <DialogTrigger
            class=" text-[#A43D3F] font-[gilroy] md:text-[45px] text-[20px]  bg-white px-5 py-2 mt-5 rounded-[20px]">
            Ro'yxatdan o'tish
        </DialogTrigger>
        <DialogContent class="bg-white w-[95%] ">
            <DialogHeader class="rounded-[10px]">

                <DialogDescription>
                    <Form />
                </DialogDescription>
            </DialogHeader>

        </DialogContent>
    </Dialog>
</template>
