<script setup>
import Banner from '@/components/Banner.vue';
import Shorten from '@/components/Shorten.vue';
import Links from '@/components/Links.vue';
import Informations from '@/components/Informations.vue';
import Boost from '@/components/Boost.vue';
</script>

<template>
  <main>
    <Banner />
    <div class="gray-background">
      <Shorten />
      <Links />
      <Informations />
      <Boost />
    </div>
  </main>
</template>

<style>
  .gray-background {
    background: var(--very-light-gray);
  }
</style>