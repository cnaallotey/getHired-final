<script setup>
import { PhBatteryPlusVertical, PhLifebuoy, PhSealCheck } from "@phosphor-icons/vue"

const points = ['Insurance','Maintenance (Service and Repairs)', 'Driver Recruitment and Management ']
</script>

<template>
  <div class="w-full mt-20 md:mt-32">
    <AppContainer>
      <div class="w-full grid lg:grid-cols-2 gap-8">
        <div class="w-full rounded-2xl overflow-hidden bg-slate-800 p-8 md:p-16 grid gap-4">
          <PhBatteryPlusVertical class="w-10 h-10 text-blue-500" />
          <p class="text-white text-xl md:text-[32px]">Worried about your EV battery wearing out?</p>
          <p class="md:text-2xl font-normal text-slate-200 max-w-lg">
            Access battery charging and pre-charged battery swap stations across Accra.
          </p>
        </div>
        <div class="w-full rounded-2xl overflow-hidden bg-slate-800 p-8 md:p-16 grid gap-4">
          <PhLifebuoy class="w-10 h-10 text-red-500" />
          <p class="text-white text-xl md:text-[32px]">Enjoy total support of your EV </p>
          <ul class="flex flex-col gap-4">
          <li v-for="point in points" class="inline-flex items-center gap-3"><PhSealCheck class="w-8 h-8 text-green-500 shrink-0" /><p class="md:text-2xl font-normal text-slate-200 max-w-lg">
           {{ point }}
          </p></li>
          </ul>
        </div>
      </div>
    </AppContainer>
  </div>
</template>
