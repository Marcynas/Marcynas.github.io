<template>
  <div
    class="lg:col-span-1 md:col-span-1 sm:col-span-3 row-span-3 h-full w-full p-4 flex flex-col justify-center align-middle"
  >
    <h1 class="font-bold text-4xl mb-2">Defeat exams</h1>
    <p class="font-bold text-xl mb-2">Website for tutors.</p>
    <p class="text-md">Made to learn vue.js</p>
    <p class="text-md">
      Sends emails using
      <a href="https://www.emailjs.com/" class="underline text-blue-500">EmailJs</a>.
    </p>
    <p class="font-bold text-xl flex flex-row w-full align-center mt-4 mb-2">Developed using:</p>
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
        <a href="https://vercel.com/">
          <img
            src="https://img.shields.io/badge/Vercel-000000.svg?style=for-the-badge&logo=Vercel&logoColor=white"
            alt="Vercel"
          />
        </a>
      </li>
      <!--https://img.shields.io/badge/Microsoft%20Outlook-0078D4.svg?style=for-the-badge&logo=Microsoft-Outlook&logoColor=white-->
      <li class="pt-2">
        <a href="https://outlook.com/">
          <img
            src="https://img.shields.io/badge/Microsoft%20Outlook-0078D4.svg?style=for-the-badge&logo=Microsoft-Outlook&logoColor=white"
            alt="Outlook"
          />
        </a>
      </li>
    </ul>
  </div>
  <div class="lg:col-span-2 md:col-span-2 sm:col-span-3 row-span-3">
    <div class="flex w-full h-full justify-center items-center align-middle">
      <iframe
        src="https://marcynas.github.io/nugalek-egzamina/"
        class="w-full h-full rounded-xl"
        scrolling="no"
        title="Nugalėk Egzaminą"
      ></iframe>
    </div>
  </div>
</template>
