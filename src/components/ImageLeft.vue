<script setup lang="ts">
import "@/assets/textcomponents.css"

type Props = {
  lang: 'de' | 'eng',
  head: string,
  text: string,
  imgSrc: string
}
const props = defineProps<Props>()
</script>

<template>
  <div class="content">
    <h2>{{ props.head }}</h2>
    <div class="content-component">
      <div class="image">
        <img :src="props.imgSrc"/>
      </div>
      <div class="content-text">
        <p class="text">{{ props.text }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>


</style>