<script setup>
import { PhLightbulbFilament, PhEnvelope } from "@phosphor-icons/vue";

const img ='https://images.pexels.com/photos/258083/pexels-photo-258083.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'
</script>

<template>
  <div class="w-full mt-32">
    <AppContainer>
      <div
        class="w-full bg-green-500 rounded-3xl overflow-hidden flex flex-col-reverse xl:flex-row items-center px-8 md:px-20 pt-8 md:pt-20 gap-x-20 gap-y-10"
      >
      <div class="bg-gray-50 rounded-t-2xl h-[300px] md:h-[400px] w-full xl:w-1/3 overflow-hidden">
      <img :src="img" class="w-full h-full object-cover object-center" alt="">
      </div>
        <div class="flex-1 flex flex-col gap-8">
          <PhLightbulbFilament class="w-10 h-10 text-amber-50" />
          <p class="text-slate-900 text-lg md:text-[32px]">
            Have a specific brand or product in mind?
          </p>
          <NuxtLink
            to="/#contact"
            class="text-white bg-slate-800 rounded-full w-fit px-8 py-4 text-semibold text-sm inline-flex items-center gap-2 whitespace-nowrap"
          >
            <span><PhEnvelope class="w-5 h-5 shrink-0" /></span>
            <span class="">Contact us</span>
          </NuxtLink>
        </div>
      </div>
    </AppContainer>
  </div>
</template>
