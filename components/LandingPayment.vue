<script setup>
import { PhCoins, PhHeadset } from "@phosphor-icons/vue";
const img ='https://images.unsplash.com/photo-1507679799987-c73779587ccf?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
</script>

<template>
  <div class="w-full mt-20 md:mt-32">
    <AppContainer>
      <div
        class="w-full bg-green-500 rounded-3xl overflow-hidden flex flex-col xl:flex-row items-center px-8 md:px-20 pt-8 md:pt-20 gap-x-20 gap-y-10"
      >
        <div class="flex-1 flex flex-col gap-8">
          <PhCoins class="w-10 h-10 text-amber-50" />
          <p class="text-slate-900 text-lg md:text-[32px] leading-normal">
            Enjoy flexible financing and pay in installments
          </p>
          <NuxtLink
            to="/#contact"
            class="text-white bg-slate-800 rounded-full w-fit px-8 py-4 text-semibold text-sm inline-flex items-center gap-2 whitespace-nowrap"
          >
            <span><PhHeadset class="w-5 h-5 shrink-0" /></span>
            <span class="">Speak to us</span>
          </NuxtLink>
        </div>
        <div class="bg-gray-50 rounded-t-2xl h-[300px] md:h-[400px] w-full xl:w-1/3 overflow-hidden">
        <img :src="img" class="w-full h-full object-cover object-center" alt="">
        </div>
      </div>
    </AppContainer>
  </div>
</template>
