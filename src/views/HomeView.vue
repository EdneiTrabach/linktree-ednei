<script setup lang="ts">
import { links } from '../config/links';
import Header from '../components/Header.vue';
import LinkButton from '../components/LinkButton.vue';
import Footer from '../components/Footer.vue';
</script>

<template>
  <div class="container py-5">
    <Header />
    <main class="d-flex flex-column align-items-center">
      <LinkButton v-for="link in links" :key="link.url" :link="link" />
    </main>
    <Footer />
  </div>
</template>