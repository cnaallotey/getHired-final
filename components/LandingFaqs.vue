<script setup>
import { PhArrowCircleUpRight, PhChatCircleText } from "@phosphor-icons/vue";
const faqs = ref([
  {
    que: "Do electric cars break down more?",
    ans: "No. EVs have fewer moving parts so they are less likely to break down.",
  },
  {
    que: "Can you buy or sell second-hand electric cars?",
    ans:
      "Yes. You can buy and sell second-hand electric cars on AutoElectriq as well as brand new electric vehicles.",
  },
  {
    que: "How long can my EV’s battery last?",
    ans:
      "Some batteries can deliver a promised range of 150,000 miles or up to 10 years.",
  },
  {
    que: "How long does it take to charge an EV battery?",
    ans:
      "For Level 1 chargers it could take a day or overnight to charge fully depending on the battery and EV model. While it could take 6-12hours for Level 2 chargers, Level 3 chargers can gain 200 miles of range with about 15 to 20 minutes of charging.",
  },
]);

const ansIndex = ref(0);
</script>

<template>
  <div id="faqs" class="w-full pt-20">
    <AppContainer>
      <div class="w-full">
        <h3 class="text-slate-900 text-xl md:text-[32px] text-center">
          <span>Frequently Asked <span class="text-green-500">Questions</span></span>
        </h3>
      </div>
      <div class="w-full grid lg:grid-cols-2 gap-8 mt-10">
        <div class="w-full grid gap-8">
          <div class="grid gap-4" v-for="(item, index) in faqs" :key="index">
            <div
              class="w-full flex items-center justify-between cursor-pointer rounded-2xl md:rounded-full p-6 select-none"
              @click="ansIndex = index"
              :class="ansIndex === index ? 'bg-green-50' : 'bg-slate-50'"
            >
              <p class="text-lg md:text-2xl font-normal text-slate-900 max-w-lg">{{ item.que }}</p>
              <PhArrowCircleUpRight
                class="w-7 h-7 shrink-0"
                :class="ansIndex === index ? 'text-green-500' : 'text-slate-500'"
              />
            </div>
            <div
            v-if="ansIndex === index"
              class="w-full bg-green-50 rounded-2xl h-full flex xl:hidden flex-col items-start justify-center p-6 gap-6 md:gap-8 md:p-8"
            >
              <PhChatCircleText class="w-10 h-10 text-green-500" />
              <p class="text-lg md:text-2xl font-normal text-slate-900 max-w-lg">
                {{ item.ans }}
              </p>
            </div>
          </div>
        </div>
        <div
          class="w-full bg-green-50 rounded-2xl h-full hidden xl:flex flex-col items-start justify-center gap-8 p-8"
        >
          <PhChatCircleText class="w-10 h-10 text-green-500" />
          <p class="text-2xl font-normal text-slate-900 max-w-lg">
            {{ faqs[ansIndex].ans }}
          </p>
        </div>
      </div>
    </AppContainer>
  </div>
</template>
