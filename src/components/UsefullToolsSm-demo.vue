<template>
  <div
    class="lg:col-span-1 md:col-span-1 sm:col-span-3 row-span-3 h-full w-full p-4 flex flex-col justify-center align-middle"
  >
    <h1 class="font-bold text-4xl mb-2">Usefull tools</h1>
    <p class="font-bold text-xl mb-2">A curated list of tools to make your life easier.</p>
    <p class="font-bold text-xl flex flex-row w-full align-center mt-4 mb-2">Built using:</p>
    <!--List-->
    <ul class="flex flex-col w-full">
      <li class="pt-2">
        <a href="https://vuejs.org/">
          <img
            src="https://img.shields.io/badge/Vue.js-4FC08D.svg?style=for-the-badge&logo=vuedotjs&logoColor=white"
            alt="Vue"
          />
        </a>
      </li>

      <li class="pt-2">
        <a href="https://tailwindcss.com/">
             <img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4.svg?style=for-the-badge&logo=Tailwind-CSS&logoColor=white" alt="Tailwind CSS"/>
        </a>
      </li>
      <li class="pt-2">
        <a href="https://workspace.google.com/products/sheets/"> 
            <img src="https://img.shields.io/badge/Google%20Sheets-34A853.svg?style=for-the-badge&logo=Google-Sheets&logoColor=white" alt="Google Sheets"/>
        </a>

      </li>
    </ul>
  </div>
  <div class="lg:col-span-2 md:col-span-2 sm:col-span-3 row-span-3">
    <div class="flex w-full h-full justify-center items-center align-middle">
      <iframe
        src="https://marcynas.github.io/usefull-tools/"
        class="w-full h-80 rounded-xl"
        scrolling="yes"
        title="Usefull Tools"
      ></iframe>
    </div>
  </div>
</template>
