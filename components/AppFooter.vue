<script setup>
import { PhFacebookLogo, PhTwitterLogo, PhInstagramLogo } from '@phosphor-icons/vue';
const socials = [
    {
        name: "Facebook",
        link: "https://facebook.com",
        icon: PhFacebookLogo
    },
    {
        name: "Twitter",
        link: "https://twitter.com",
        icon: PhTwitterLogo
    },
    {
        name: "Instagram",
        link: "https://instagram.com",
        icon: PhInstagramLogo
    },
]
</script>

<template>
    <div class="w-full py-12 md:py-20 bg-slate-800 mt-20 md:mt-32">
        <AppContainer>
        <div class="w-full flex items-center justify-center flex-col md:flex-row flex-wrap gap-8 md:gap-5 md:justify-between">
            <NuxtLink to="/#top">
            <NuxtImg src="/images/logo.svg" class="w-8 h-8" />
          </NuxtLink>
          <div class="flex items-center gap-5 w-fit">
          <NuxtLink v-for="item in socials" :to="item.link" class="text-white hover:text-green-500" target="_blank">
          <Component :is="item.icon" class="w-7 h-7 shrink-0" />
          <span class="sr-only">{{ item.name }}</span>
          </NuxtLink>
          </div>
          <p class="text-white">All Rights Reserved © DriveGo Inc</p>
        </div>
        </AppContainer>
    </div>
</template>