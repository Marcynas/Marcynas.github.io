<script setup>
import { ref } from 'vue'
import OrelisSmDemo from '@/components/OrelisSm-demo.vue'
import NugEgSmDemo from '@/components/NugEgSm-demo.vue'
import TikChatSmDemo from '@/components/TikChatSm-demo.vue'

const names = ref(['Orelis', 'Nugalėk egzaminą', 'TikChat'])
const selectedName = ref(names.value[0])

const nextName = () => {
  const index = names.value.indexOf(selectedName.value)
  if (index === names.value.length - 1) {
    selectedName.value = names.value[0]
  } else {
    selectedName.value = names.value[index + 1]
  }
}

const prevName = () => {
  const index = names.value.indexOf(selectedName.value)
  if (index === 0) {
    selectedName.value = names.value[names.value.length - 1]
  } else {
    selectedName.value = names.value[index - 1]
  }
}
</script>

<template>
  <section
    class="flex flex-col items-center justify-center self-center z-10 select-none"
    id="projects"
  >
    <div class="flex flex-row justify-center items-center mb-4">
      <div class="col-span-1 row-span-1 h-full flex justify-center">
        <img class="h-24 animate-blob4" src="@/assets/blob1.svg" alt="blob1" />
      </div>
      <div class="col-span-2 row-span-1 flex justify-start">
        <p class="text-5xl font-bold align-middle self-center">Projects</p>
      </div>
    </div>

    <div class="flex flex-row justify-center items-center">
      <div
        class="flex justify-center items-center rounded-full border-2 p-2 border-black mr-6 hover:bg-black hover:text-white cursor-pointer transition duration-500 ease-in-out"
        v-on:click="prevName"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="size-6"
        >
          <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5 8.25 12l7.5-7.5" />
        </svg>
      </div>
      <div
        class="flex justify-center items-center rounded-full border-2 p-2 border-black ml-6 hover:bg-black hover:text-white cursor-pointer transition duration-500 ease-in-out"
        v-on:click="nextName"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="size-6"
        >
          <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
        </svg>
      </div>
    </div>

    <div class="mt-4">
      <OrelisSmDemo v-if="selectedName === 'Orelis'" />
      <NugEgSmDemo v-else-if="selectedName === 'Nugalėk egzaminą'" />
      <TikChatSmDemo v-else-if="selectedName === 'TikChat'" />
      <div class="col-span-3 row-span-1 h-64 flex justify-center" v-else>
        <p class="text-5xl font-bold align-middle self-center animate-pulse">
          More comming soon...
        </p>
      </div>
    </div>
  </section>
</template>
