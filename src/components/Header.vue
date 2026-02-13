<script setup lang="ts">
const props = defineProps<{ lang: 'de' | 'eng' }>()
const emit = defineEmits<{ (e: 'toggle-lang'): void }>()
</script>

<template>
  <header class="header-bar page">
    <div class="lang-switch">
      <span
        class="lang-item"
        @click="emit('toggle-lang')"
      >DE</span>
      <span class="separator"> | </span>
      <span
        class="lang-item"
        @click="emit('toggle-lang')"
      >EN</span>
    </div>
  </header>
</template>

<style scoped>
.header-bar {
  display: flex;
  justify-content: flex-end;
  padding-top: 1em;
  padding-bottom: 0em;
  padding-right: 1em;
  margin-bottom: 0em;
}

.lang-switch {
  font-family: 'Bebas Neue', sans-serif;
  font-weight: 700;
  font-size: 2rem;
  color: #0A4152;
}

.lang-item {
  cursor: pointer;
}

.lang-item:hover {
  text-decoration: underline;
}

.separator {
  cursor: default;
}
</style>