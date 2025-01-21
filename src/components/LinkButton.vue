<script setup lang="ts">
import { Link } from '../config/links';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

defineProps<{
  link: Link;
}>();
</script>

<template>
  <a :href="link.url" target="_blank" rel="noopener noreferrer" class="link-button">
    <FontAwesomeIcon :icon="['fab', link.icon]" v-if="link.icon !== 'globe' && link.icon !== 'envelope'" />
    <FontAwesomeIcon :icon="['fas', link.icon]" v-else />
    <span>{{ link.name }}</span>
  </a>
</template>

<style lang="scss" scoped>
.link-button {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  margin: 0.5rem 0;
  background-color: var(--bs-light);
  border-radius: 0.5rem;
  text-decoration: none;
  color: var(--bs-dark);
  transition: transform 0.2s, box-shadow 0.2s;
  width: 100%;
  max-width: 400px;

  &:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  }

  span {
    font-weight: 500;
  }
}

[data-bs-theme="dark"] .link-button {
  background-color: var(--bs-dark);
  color: var(--bs-light);
}
</style>