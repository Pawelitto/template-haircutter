<script setup lang="ts">
const { data: page } = await useAsyncData("index", () =>
  queryContent("/").findOne()
);

useSeoMeta({
  title: page.value.title,
  ogTitle: page.value.title,
  description: page.value.description,
  ogDescription: page.value.description,
});

const items = [
  "https://media.students.pl/public/article/image/fryzjer.jpeg",
  "https://www.themailroombarberco.com/cdn/shop/articles/MailroomBarberCo_TeachingSession-7_2048x.jpg?v=1642018666",
  "https://gfx.stylzycia.radiozet.pl/var/g3-radiozetstylzycia/storage/images/moda-i-uroda/fryzjerka-z-leborka-zniszczyla-klientce-wlosy-sad-zarzadzil-odszkodowanie/14712729-1-pol-PL/Fryzjerka-z-Leborka-zniszczyla-klientce-wlosy.-Sad-zarzadzil-odszkodowanie_full-hd.jpg",
  "https://porady.pracuj.pl/file/2021/06/fryzjer_900.jpg",
  "https://d-art.ppstatic.pl/kadry/k/r/1/72/ec/a1ac1b6122007d1bbd7de11bd4e1_o_original.jpg",
  "https://kwalifikacje.edu.pl/wp-content/uploads/shutterstock_481482805-scaled.jpg",
];
</script>

<template>
  <div>
    <ULandingHero
      :title="page.hero.title"
      :description="page.hero.description"
      :links="page.hero.links"
    >
      <template #headline>
        <UBadge
          v-if="page.hero.headline"
          variant="subtle"
          size="lg"
          class="relative rounded-full font-semibold"
        >
          <NuxtLink :to="page.hero.headline.to" class="focus:outline-none">
            <span class="absolute inset-0" aria-hidden="true" />
          </NuxtLink>

          {{ page.hero.headline.label }}

          <UIcon
            v-if="page.hero.headline.icon"
            :name="page.hero.headline.icon"
            class="ml-1 w-4 h-4 pointer-events-none"
            dynamic
          />
        </UBadge>
      </template>

      <UCarousel
        v-slot="{ item }"
        :items="items"
        :ui="{ item: 'basis-full ' }"
        :prev-button="{
          color: 'gray',
          icon: 'i-heroicons-arrow-left-20-solid',
        }"
        :next-button="{
          color: 'gray',
          icon: 'i-heroicons-arrow-right-20-solid',
        }"
        arrows
        class="rounded-lg overflow-hidden max-h-[85vh]"
      >
        <NuxtImg
          :src="item"
          :alt="item"
          class="w-full object-cover"
          loading="lazy"
          draggable="false"
        />
      </UCarousel>
    </ULandingHero>

    <ULandingSection
      :title="page.offer.title"
      :description="page.offer.description"
      :headline="page.offer.headline"
    >
      <UPageGrid
        id="oferta"
        class="scroll-mt-[calc(var(--header-height)+140px+128px+96px)]"
      >
        <ULandingCard
          v-for="(item, index) in page.offer.items"
          :key="index"
          v-bind="item"
        />
      </UPageGrid>
    </ULandingSection>

    <ULandingSection
      :headline="page.testimonials.headline"
      :title="page.testimonials.title"
      :description="page.testimonials.description"
    >
      <UPageColumns
        id="opinie"
        class="xl:columns-4 scroll-mt-[calc(var(--header-height)+140px+128px+96px)]"
      >
        <div
          v-for="(testimonial, index) in page.testimonials.items"
          :key="index"
          class="break-inside-avoid"
        >
          <ULandingTestimonial v-bind="testimonial" />
        </div>
      </UPageColumns>
    </ULandingSection>

    <ULandingSection id="kontakt" class="scroll-mt-[var(--header-height)]">
      <Kontakt />
    </ULandingSection>

    <ULandingSection
      id="faq"
      :title="page.faq.title"
      :description="page.faq.description"
      class="-scroll-mt-[var(--header-height)]"
    >
      <ULandingFAQ
        multiple
        :items="page.faq.items"
        :ui="{
          button: {
            label: 'font-semibold',
            trailingIcon: {
              base: 'w-6 h-6',
            },
          },
        }"
        class="max-w-4xl mx-auto"
      />
    </ULandingSection>
  </div>
</template>
