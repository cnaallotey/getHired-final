<script setup>
const vehicles = [
    {
        name: 'Two - Wheelers ',
        subtext: 'Bikes and Scooters',
        slug:'motor'

    },
    {
        name: 'Three - Wheelers ',
        subtext: 'Keke / Pragya',
        slug:'pragya'

    },{
        name: 'Cars',
        subtext: '',
        slug:'car'

    }
]
</script>

<template>
    <div class="w-full mt-20 md:mt-32">
        <AppContainer>
        <div class="w-full flex flex-col gap-10">
            <h3 class="text-slate-900 text-lg md:text-[32px] text-center"><span>Choose from list of <span class="text-green-500">Electric Vehicles available</span></span></h3>
        <div class="w-full grid xl:grid-cols-3 gap-8">
        <div v-for="item in vehicles" :key="item.slug" class="w-full bg-slate-800 p-8 rounded-3xl overflow-hidden flex justify-between flex-col items-center text-center">
           <div class="flex flex-col item-center gap-1"> <p class="text-white text-2xl">{{ item.name }}</p>
            <p class="text-slate-200">{{ item.subtext }}</p></div>
            <img :src="`/images/${item.slug}.png`" class="w-auto pointer-events-none" :alt="item.slug">
            <div class="w-3 h-5 shrink-0"></div>
        </div>
        </div>
        
        </div>
        </AppContainer>
    </div>
</template>