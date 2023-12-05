<script setup>
import { PhHeart } from '@phosphor-icons/vue';
const img = 'https://images.pexels.com/photos/110844/pexels-photo-110844.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'
</script>

<template>
    <div class="w-full mt-20 md:mt-32">
        <AppContainer>
        <div class="w-full bg-green-500 rounded-3xl overflow-hidden flex flex-col-reverse xl:flex-row items-center px-8 md:px-20 pt-8 md:pt-20 gap-x-20 gap-y-10">
        <div class="bg-gray-50 rounded-t-2xl h-[300px] md:h-[400px] w-full xl:w-1/3 overflow-hidden">
        <img :src="img" class="w-full h-full object-cover" alt="">
        </div>
        <div class="flex-1 flex flex-col gap-8">
        <PhHeart class="w-8 h-8 text-rose-50" />
        <p class="text-slate-900 text-lg md:text-[32px] leading-normal">A trusted friend with years of experience in deploying EV businesses across Africa</p>
        </div>
        </div>
        </AppContainer>
    </div>
</template>