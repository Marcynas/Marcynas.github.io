<script setup>
import { ref } from 'vue'
import OrelisFullDemo from '@/components/OrelisFull-demo.vue'
import NugEgFullDemo from '@/components/NugEgFull-demo.vue'
import TikChatFullDemo from '@/components/TikChatFull-demo.vue'
import UsefullToolsFullDemo from '@/components/UsefullToolsFull-demo.vue'

const names = ref(['Nugalėk egzaminą','Orelis', 'Usefull tools' , 'TikChat'])
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

//monitoring screen size
const isMobile = ref(window.innerWidth < 768)
window.addEventListener('resize', () => {
  isMobile.value = window.innerWidth < 768
})
</script>

<template>
  <main>
    <div class="absolute top-0 left-0 select-none block">
      <div class="w-screen h-screen grid gap-4 grid-cols-3">
        <!-- Projects -->
        <div class="flex justify-center items-center col-span-3 ml-32">
          <p
            v-if="!isMobile"
            class="animate-blob1 select-none text-4xl font-bold text-black absolute z-10 hover:text-white cursor-pointer transition duration-500 ease-in-out"
            onclick="document.getElementById('projects').scrollIntoView({ behavior: 'smooth' })"
          >
            Projects
          </p>
          <RouterLink
            v-else
            class="animate-blob1 select-none text-4xl font-bold text-black absolute z-10 hover:text-white cursor-pointer transition duration-500 ease-in-out"
            to="/projects"
          >
            Projects
          </RouterLink>

          <img class="animate-blob1 h-96" src="@/assets/blob1.svg" alt="blob1" />
        </div>
        <div class="col-span-2" v-if="!isMobile"></div>
        <div class="flex justify-center items-center col-span-2" v-if="isMobile">
          <p
            v-if="!isMobile"
            class="animate-blob3 select-none text-4xl font-bold text-black absolute z-10 hover:text-white cursor-pointer transition duration-500 ease-in-out"
            onclick="document.getElementById('Socials').scrollIntoView({ behavior: 'smooth' })"
          >
            Socials
          </p>
          <RouterLink
            v-else
            class="animate-blob3 select-none text-4xl font-bold text-black absolute z-10 hover:text-white cursor-pointer transition duration-500 ease-in-out"
            to="/socials"
          >
            Socials
          </RouterLink>
          <img class="animate-blob3 h-52" src="@/assets/blob3.svg" alt="blob3" />
        </div>
        <div class="flex justify-center items-center col-span-1">
          <p
            v-if="!isMobile"
            class="animate-blob2 select-none text-4xl font-bold text-black absolute z-10 hover:text-white cursor-pointer transition duration-500 ease-in-out"
            onclick="document.getElementById('about').scrollIntoView({ behavior: 'smooth' })"
          >
            About
          </p>
          <RouterLink
            v-else
            class="animate-blob2 select-none text-4xl font-bold text-black absolute z-10 hover:text-white cursor-pointer transition duration-500 ease-in-out"
            to="/about"
          >
            About
          </RouterLink>
          <img class="animate-blob2 h-60" src="@/assets/blob2.svg" alt="blob2" />
        </div>
        <div class="col-span-1"></div>
        <div class="flex justify-center items-center col-span-2" v-if="!isMobile">
          <p
            class="animate-blob3 select-none text-4xl font-bold text-black absolute z-10 hover:text-white cursor-pointer transition duration-500 ease-in-out"
            onclick="document.getElementById('Socials').scrollIntoView({ behavior: 'smooth' })"
          >
            Socials
          </p>

          <img class="animate-blob3 h-52" src="@/assets/blob3.svg" alt="blob3" />
        </div>
      </div>
    </div>
    <section
      class="flex flex-col h-screen w-screen overflow-hidden items-center pr-32 pl-5 justify-center z-10"
    >
      <div class="flex flex-col items-center justify-center z-10 font-sans">
        <div>
          <h1 class="text-4xl font-bold">Hi, I'm Martynas.</h1>
          <p class="text-2xl sm:text-2xl font-bold">Explore My Work and Passion</p>
        </div>
      </div>
    </section>
    <section
      v-if="!isMobile"
      class="flex h-screen w-screen items-center justify-center self-center z-10 select-none overflow-hidden"
      id="projects"
    >
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
      <div class="grid grid-cols-3 grid-rows-4 gap-4 h-3/4 w-3/4">
        <div class="col-span-1 row-span-1 h-full flex justify-center">
          <img class="h-full animate-blob4" src="@/assets/blob1.svg" alt="blob1" />
        </div>
        <div class="col-span-2 row-span-1 flex justify-start">
          <p class="text-5xl font-bold align-middle self-center">Projects</p>
        </div>
        <OrelisFullDemo v-if="selectedName === 'Orelis'" />
        <NugEgFullDemo v-else-if="selectedName === 'Nugalėk egzaminą'" />
        <TikChatFullDemo v-else-if="selectedName === 'TikChat'" />
        <UsefullToolsFullDemo v-else-if="selectedName === 'Usefull tools'" />
        <div class="col-span-3 row-span-1 h-64 flex justify-center" v-else>
          <p class="text-5xl font-bold align-middle self-center animate-pulse">
            More comming soon...
          </p>
        </div>
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
    </section>
    <section
      v-if="!isMobile"
      class="select-none flex h-screen w-screen items-center justify-center self-center z-10 overflow-hidden"
      id="about"
    >
      <div class="grid grid-cols-3 grid-rows-4 gap-4 h-3/4 w-3/4 rounded-xl p-4">
        <div class="col-span-2 row-span-1 flex justify-end">
          <p class="text-4xl font-bold align-middle self-center">About</p>
        </div>
        <div class="col-span-1 row-span-1 h-full flex justify-center">
          <img class="h-full animate-blob4" src="@/assets/blob2.svg" alt="blob2" />
        </div>
        <div
          class="lg:col-span-1 row-span-3 p-4 flex flex-col justify-center align-middle h-fit w-full"
        >
          <img class="rounded-lg" src="@/assets/profile.jpg" alt="profile" />
        </div>
        <div
          class="flex flex-col w-full h-full col-span-2 row-span-3 p-4 justify-center text-justify"
        >
          <p class="font-bold text-xl flex flex-row w-full align-center mt-4 mb-2">
            Hi 👋, I'm Martynas!
          </p>
          <p>I'm a Data Engineer at IBM and an Information Systems student at KTU.</p>
          <p class="flex flex-row w-full align-center mt-4 mb-2">
            Various courses in my major required extensive knowledge in data engineering tools and
            methodologies, such as applying Relational Database Theory and SQL, defining reports and
            dashboards for BI and data mining tasks, utilising data and databases for domain
            analysis and decision-making support.
          </p>
          <p class="flex flex-row w-full align-center mt-4 mb-2">
            My understanding of Object-Oriented Programming in Java/C# helps me to see the wider
            picture and design various tools to help with data analysis and visualisation. I'm
            comfortable with both Agile and Waterfall project management methodologies, and I'm
            always looking to learn new tools and skills.
          </p>
          <p class="font-bold text-xl flex flex-row w-full align-center mt-4 mb-2">Skills:</p>
          <p>Vue.js, Python, Databricks, Azure.</p>
        </div>
      </div>
    </section>
    <section
      v-if="!isMobile"
      class="flex flex-col h-screen h-screen w-screen items-center self-center z-10 select-none overflow-hidden"
      id="Socials"
    >
      <div class="absolute flex flex-row h-2/3 justify-center align-middle">
        <img class="animate-blob5" src="@/assets/blob3.svg" alt="blob3" />
      </div>

      <div class="flex flex-row h-1/2 justify-center align-middle mt-12">
        <div class="flex flex-col items-center justify-center z-10 font-sans">
          <a href="https://github.com/Marcynas">
            <img class="h-32 m-4" src="@/assets/github-mark.svg" alt="GitHub" />
          </a>
          <p>@Marcynas</p>
        </div>

        <div class="flex flex-col items-center justify-center z-10 font-sans">
          <a href="https://linkedin.com/in/martynas-tvaska">
            <img class="h-32 m-4" src="@/assets/linkedin-mark.svg" alt="LinkedIn" />
          </a>
          <p>@Martynas-Tvaska</p>
        </div>

        <div class="flex flex-col items-center justify-center z-10 font-sans">
          <a href="https://www.credly.com/users/martynas-tvaska/badges">
            <img class="h-32 m-4" src="@/assets/credly-mark.svg" alt="Credly" />
          </a>
          <p>@Martynas-Tvaska</p>
        </div>
      </div>
      <footer class="z-10 font-sans mt-32">
        <p>See you soon 👋</p>
      </footer>
    </section>
  </main>
</template>

<style scoped>
.animate-blob1 {
  animation: move 3s infinite;
  animation-timing-function: linear;
}
.animate-blob2 {
  animation: move 2s infinite;
  animation-timing-function: linear;
}
.animate-blob3 {
  animation: move 4s infinite;
  animation-timing-function: linear;
}

/* animation move */

@keyframes move {
  0% {
    transform: translateY(0);
  }
  25% {
    transform: translateY(-10px);
  }
  50% {
    transform: translateY(0);
  }
  75% {
    transform: translateY(10px);
  }
  100% {
    transform: translateY(0);
  }
}

/* animation wigle */

@keyframes wiggle {
  0% {
    transform: rotate(0deg);
  }
  25% {
    transform: rotate(10deg);
  }
  50% {
    transform: rotate(0deg);
  }
  75% {
    transform: rotate(-10deg);
  }
  100% {
    transform: rotate(0deg);
  }
}
</style>
