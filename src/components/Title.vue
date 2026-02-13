<script setup lang="ts">
import { computed } from 'vue'

type Props = {
  lang: 'de' | 'eng'
}

const props = defineProps<Props>()

const titleText = computed(() =>
  props.lang === 'eng'
    ? 'On the Spectrum<br> & in IT'
    : 'Auf dem Spektrum<br> & in der IT'
)
</script>

<template>
  <div class="header">
    <h1 v-html="titleText"></h1>
  </div>
</template>

<style scoped>
</style>