<template>
  <div
    class="text-center md:grid md:grid-cols-2 lg:grid-cols-3 md:gap-12 md:space-y-0"
  >
    <div>
      <div
        class="flex justify-center items-center mx-auto mb-4 w-10 h-10 bg-gray-100 rounded-lg dark:bg-gray-800 lg:h-16 lg:w-16"
      >
        <UIcon
          name="i-heroicons-envelope"
          class="w-5 h-5 text-gray-600 lg:w-8 lg:h-8 dark:text-gray-500"
          dynamic
        />
      </div>
      <p class="mb-2 text-xl font-bold dark:text-white">Napisz do nas:</p>
      <p class="mb-3 text-gray-500 dark:text-gray-400">
        Napisz do nas, aby uzyskać odpowiedzi na swoje pytania i zapytania.
      </p>
      <NuxtLink
        to="mailto:abc@example.com"
        class="font-semibold text-primary-600 dark:text-primary-500 hover:underline"
        >hello@flowbite.com</NuxtLink
      >
    </div>
    <div>
      <div
        class="flex justify-center items-center mx-auto mb-4 w-10 h-10 bg-gray-100 rounded-lg dark:bg-gray-800 lg:h-16 lg:w-16"
      >
        <UIcon
          name="i-heroicons-phone"
          class="w-5 h-5 text-gray-600 lg:w-8 lg:h-8 dark:text-gray-500"
          dynamic
        />
      </div>
      <p class="mb-2 text-xl font-bold dark:text-white">Zadzwoń pod:</p>
      <p class="mb-3 text-gray-500 dark:text-gray-400">
        Chętnie odpowiemy na Twoje pytania i zapytania telefonicznie.
      </p>
      <NuxtLink
        to="tel:+48605898932"
        class="font-semibold text-primary-600 dark:text-primary-500"
        >+48 605 898 932</NuxtLink
      >
    </div>
    <div>
      <div
        class="flex justify-center items-center mx-auto mb-4 w-10 h-10 bg-gray-100 rounded-lg dark:bg-gray-800 lg:h-16 lg:w-16"
      >
        <UIcon
          name="i-heroicons-map-pin"
          class="w-5 h-5 text-gray-600 lg:w-8 lg:h-8 dark:text-gray-500"
          dynamic
        />
      </div>
      <p class="mb-2 text-xl font-bold dark:text-white">Lokalizacja</p>
      <p class="mb-3 text-gray-500 dark:text-gray-400">
        Sprawdź naszą lokalizację i odwiedź nas w dogodnym dla Ciebie terminie.
      </p>
      <NuxtLink
        to="https://www.google.com/maps/dir/50.1555787,18.6642136/Fryzjer+Sabina+Baron,+Zwyci%C4%99stwa+16,+43-178+Ornontowice/@50.1589583,18.6313381,12z/data=!3m1!4b1!4m18!1m7!3m6!1s0x4711353c44b9fb09:0xf496449b6f1540c0!2sFryzjer+Sabina+Baron!8m2!3d50.1810319!4d18.7642638!16s%2Fg%2F11fzfdsg6c!4m9!1m1!4e1!1m5!1m1!1s0x4711353c44b9fb09:0xf496449b6f1540c0!2m2!1d18.764198!2d50.1810087!3e0?entry=ttu"
        target="_blank"
        class="inline-flex py-2 px-4 text-sm font-medium text-center rounded-lg border text-primary-600 border-primary-600 hover:text-white hover:bg-primary-600 focus:ring-4 focus:outline-none focus:ring-primary-300 dark:border-primary-500 dark:text-primary-500 dark:hover:text-white dark:hover:bg-primary-600 dark:focus:ring-primary-800"
        >Zobacz na mapie</NuxtLink
      >
    </div>
  </div>
</template>