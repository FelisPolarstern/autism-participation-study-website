<script setup lang="ts">
import { ref } from "vue";
import MainContent from "@/components/MainContent.vue";
import Title from "@/components/Title.vue";
import Header from "@/components/Header.vue"
import Impressum from "@/components/Impressum.vue";

const lang = ref<'de' | 'eng'>('de');

function toggleLang() {
  lang.value = lang.value === 'de' ? 'eng' : 'de';
}
</script>

<template>
  <Header :lang="lang" @toggle-lang="toggleLang"  />

  <Title :lang="lang"/>
  <MainContent :lang="lang" />
  <Impressum :lang="lang" />
</template>

<style scoped>

</style>