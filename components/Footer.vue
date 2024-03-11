<script setup lang="ts">
const links = [
  {
    label: "Resources",
    to: "/resources",
  },
  {
    label: "Features",
    to: "/features",
  },
  {
    label: "Company",
    to: "/company",
  },
];

const toast = useToast();

const email = ref("");
const loading = ref(false);

function onSubmit() {
  loading.value = true;

  setTimeout(() => {
    toast.add({
      title: "Subscribed!",
      description: "You've been subscribed to our newsletter.",
    });

    loading.value = false;
  }, 1000);
}
</script>

<template>
  <UFooter>
    <template #top>
      <UFooterColumns :links="links">
        <template #right> </template>
      </UFooterColumns>
    </template>

    <template #left>
      <p class="text-gray-500 dark:text-gray-400 text-sm">
        Copyright © {{ new Date().getFullYear() }}. All rights reserved.
      </p>
    </template>

    <template #center>
      <p>Stworzone przez:&nbsp;</p>
      <NuxtLink
        to="https://github.com/Pawelitto"
        target="_blank"
        class="text-primary-500 dark:text-primary-400 font-bold"
      >
        Paweł Pietras</NuxtLink
      >
    </template>

    <template #right>
      <UColorModeButton size="sm" />
    </template>
  </UFooter>
</template>
