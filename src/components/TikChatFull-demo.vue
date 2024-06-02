<template>
  <div
    class="lg:col-span-1 md:col-span-1 sm:col-span-3 row-span-3 h-full w-full p-4 flex flex-col justify-center align-middle"
  >
    <h1 class="font-bold text-4xl mb-2">TikChat</h1>
    <p class="font-bold text-xl mb-2">Chat PWA.</p>
    <p class="text-md">Made as a university project</p>
    <p class="font-bold mt-2">Avavlible functions:</p>
    <ul class="list-disc list-inside">
      <li>🔒 Secure login.</li>
      <li>📱 Cross-platform support</li>
      <li>💬 Ability to chat anonymously.</li>
      <li>🖼 Send images.</li>
      <li>🕵️ Private messages.</li>
      <li>🫂 Friend list.</li>
      <li>❗ Profile editing.</li>
    </ul>
    <p class="font-bold text-xl flex flex-row w-full align-center mt-4 mb-2">Developed using:</p>
    <!--List-->
    <ul class="flex flex-col w-full">
      <li class="pt-2">
        <a href="https://firebase.google.com/">
          <img
            src="https://img.shields.io/badge/Firebase-FFCA28.svg?style=for-the-badge&logo=Firebase&logoColor=black"
            alt="Firebase"
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
        <a href="https://reactjs.org/">
          <img
            src="https://img.shields.io/badge/React-61DAFB.svg?style=for-the-badge&logo=React&logoColor=black"
            alt="React"
          />
        </a>
      </li>
    </ul>
  </div>
  <div class="lg:col-span-2 md:col-span-2 sm:col-span-3 row-span-3">
    <div class="flex w-full h-full justify-center items-center align-middle">
      <iframe
        src="https://tik-chat.vercel.app/"
        class="w-full h-full rounded-xl"
        title="TickChat"
      ></iframe>
    </div>
  </div>
</template>
