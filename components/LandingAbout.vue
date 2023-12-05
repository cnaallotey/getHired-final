<script setup>
import { PhTimer, PhHandCoins, PhFactory } from "@phosphor-icons/vue";
const points = [
  {
    slug: PhTimer,
    message:
      "You no longer have to wait at petrol stations. You can charge your EV at home.",
      color: 'bg-orange-50 text-orange-500'
  },
  {
    slug: PhHandCoins,
    message:
      "Cost of electricity for charging an EV is less than the cost of petrol used for a similar vehicle that’s traveling the same distance.",
      color: 'text-blue-500 bg-blue-50'
  },
  {
    slug: PhFactory,
    message:
      "Carbon emissions of an electric vehicle is lesser than that of a petrol or diesel car which makes the environment safe. ",
      color: 'text-green-500 bg-green-50'
  },
];
</script>

<template>
  <div class="w-full mt-20 md:mt-32">
    <AppContainer>
      <div class="w-full grid lg:grid-cols-3 gap-x-20 gap-y-8">
        <div
          v-for="(item, index) in points"
          :key="index"
          class="w-full rounded-xl p-8 grid gap-8"
          :class="item.color"
        >
          <Component :is="item.slug" class="w-8 h-8"></Component>
          <p class="text-lg md:text-2xl text-slate-900">{{ item.message }}</p>
        </div>
      </div>
    </AppContainer>
  </div>
</template>
