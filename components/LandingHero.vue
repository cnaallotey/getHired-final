<script setup>
import { PhArrowUpRight, PhChatCenteredDots, PhLightning } from "@phosphor-icons/vue";
</script>

<template>
  <div class="w-full mt-16 md:mt-32">
    <AppContainer>
      <div class="w-full flex flex-col items-center gap-10">
        <PhArrowUpRight class="text-slate-600" :size="32" />
        <h1 class="text-[30px] md:text-[50px] font-semibold text-slate-900 text-center max-w-5xl">
          All in one platform to
          <span class="text-green-500">buy and maintain EV vehicles</span> from vetted
          suppliers, secure <span class="text-green-500">flexible financing, maintenance</span> and <span class="text-green-500">insurance</span>.
        </h1>
        <NuxtLink to="/#contact" class="text-white bg-slate-800 rounded-full px-8 py-4 text-semibold text-sm inline-flex items-center gap-2 whitespace-nowrap">
        <span><PhChatCenteredDots class="w-5 h-5 shrink-0" /></span>
        <span class="">Speak to an expert</span>
        </NuxtLink>
      </div>
    </AppContainer>
  </div>
  <div class="mt-20 md:mt-32 w-full bg-slate-800 py-6 md:py-8 gap-5">
 <ClientOnly>
    <Vue3Marquee>
        <div v-for="x in 10" class="inline-flex px-5 items-center gap-2 text-green-500">
        <span><PhLightning class="w-5 h-5md:w-8 md:h-8 shrink-0" /></span>
        <span class="text-lg md:text-xl font-semibold">The Future is Electric</span>
        </div>
  </Vue3Marquee>
 </ClientOnly>
  
  </div>
</template>
