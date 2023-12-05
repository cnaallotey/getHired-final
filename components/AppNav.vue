<script setup>
import { PhList, PhChatCenteredDots } from "@phosphor-icons/vue";
const navLinks = [
  {
    name: "Services",
    link: "/#services",
  },
  {
    name: "Frequently Asked Questions",
    link: "/#faqs",
  },
];
</script>

<template>
  <div class="w-full py-4 bg-white/50 backdrop-blur-xl">
    <AppContainer>
      <div class="w-full flex justify-between">
        <div class="flex items-center gap-2">
          <NuxtLink to="/#top">
            <NuxtImg src="/images/logo.svg" class="w-8 h-8" />
          </NuxtLink>
        </div>
        <div class="flex items-center gap-10">
        <div class="flex items-center gap-5 xl:gap-10">
        <NuxtLink v-for="(item, index) in navLinks" :key="index" :to="item.link" class="text-sm text-slate-500 hover:text-emerald-500 hidden md:inline-flex">
        {{ item.name }}
        </NuxtLink>
        <NuxtLink to="/#contact" class="text-white bg-slate-800 rounded-full px-8 py-4 text-semibold text-sm inline-flex items-center gap-2 whitespace-nowrap">
        <span><PhChatCenteredDots class="w-5 h-5 shrink-0" /></span>
        <span class="sr-only md:not-sr-only">Speak to an expert</span>
        </NuxtLink>
        </div>
        </div>
      </div>
    </AppContainer>
  </div>
</template>
