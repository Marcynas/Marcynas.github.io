<template>
  <div
    class="lg:col-span-1 md:col-span-1 sm:col-span-3 row-span-3 h-full w-full p-4 flex flex-col justify-center align-middle"
  >
    <h1 class="font-bold text-4xl mb-2">Orelis</h1>
    <p class="font-bold text-xl mb-2">Simple weather app.</p>
    <p class="text-md">Made to learn vue.js</p>
    <p class="text-md">
      Displays weather data from
      <a href="https://www.weatherapi.com/" class="underline text-blue-500">WeatherApi</a>.
    </p>
    <p class="text-md">
      Retrieves location using
      <a href="https://vueuse.org/" class="underline text-blue-500">VueUse</a>.
    </p>
    <p class="text-md">
      Icons from
      <a href="https://github.com/basmilius/weather-icons" class="underline text-blue-500"
        >Meteocons</a
      >.
    </p>
    <p class="font-bold text-xl flex flex-row w-full align-center mt-4 mb-2">Developed using:</p>
    <!--List-->
    <ul class="flex flex-col w-full">
      <li class="">
        <a href="https://vitejs.dev/">
          <img
            src="https://img.shields.io/badge/Vite-646CFF.svg?style=for-the-badge&logo=Vite&logoColor=white"
            alt="Vite"
          />
        </a>
      </li>
      <li class="pt-2">
        <a href="https://vuejs.org/">
          <img
            src="https://img.shields.io/badge/Vue.js-4FC08D.svg?style=for-the-badge&logo=vuedotjs&logoColor=white"
            alt="Vue"
          />
        </a>
      </li>

      <li class="pt-2">
        <a href="https://vercel.com/">
          <img
            src="https://img.shields.io/badge/Vercel-000000.svg?style=for-the-badge&logo=Vercel&logoColor=white"
            alt="Vercel"
          />
        </a>
      </li>

      <li class="pt-2">
        <a href="https://tailwindcss.com/">
          <img
            src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4.svg?style=for-the-badge&logo=Tailwind-CSS&logoColor=white"
            alt="Tailwind"
          />
        </a>
      </li>
    </ul>
  </div>
  <div class="lg:col-span-2 md:col-span-2 sm:col-span-3 row-span-3">
    <div class="flex w-full h-full justify-center items-center align-middle">
      <iframe
        src="https://orelis.vercel.app/"
        class="w-full h-full rounded-xl"
        allow="geolocation"
        title="Orelis"
      ></iframe>
    </div>
  </div>
</template>
