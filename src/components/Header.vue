<script setup lang="ts">
import { ref } from 'vue';

const isDarkMode = ref(false);

const toggleTheme = () => {
  isDarkMode.value = !isDarkMode.value;
  document.documentElement.setAttribute('data-bs-theme', isDarkMode.value ? 'dark' : 'light');
};
</script>

<template>
  <header class="text-center mb-4">
    <div class="avatar-container mb-3">
      <img src="/src/assets/img/imagem1.jpeg" alt="Profile Avatar" class="avatar" />
    </div>
    <h1 class="mb-2">Ednei Trabach</h1>
    <p class="text-muted">Developer | Frontend | Backend | Fullstack </p>
    <button @click="toggleTheme" class="theme-toggle">
      <FontAwesomeIcon :icon="['fas', isDarkMode ? 'sun' : 'moon']" />
    </button>
  </header>
</template>

<style lang="scss" scoped>
.avatar-container {
  width: 150px;
  height: 150px;
  margin: 0 auto;
  overflow: hidden;
  border-radius: 50%;
  border: 3px solid var(--bs-primary);
}

.avatar {
  width: 100%;
  height: 100%;
  object-fit: contain;
  scale: 1.5;
  top: 30px;
  position: relative;
}

.theme-toggle {
  position: fixed;
  top: 1rem;
  right: 1rem;
  padding: 0.5rem;
  border-radius: 50%;
  border: none;
  background: var(--bs-light);
  cursor: pointer;
  transition: transform 0.2s;

  &:hover {
    transform: scale(1.1);
  }
}

[data-bs-theme="dark"] .theme-toggle {
  background: var(--bs-dark);
  color: var(--bs-light);
}
</style>