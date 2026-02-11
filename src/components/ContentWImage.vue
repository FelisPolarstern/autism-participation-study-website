<script setup lang="ts">

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
    <div class="content-component">
      <div class="image">
        <img :src="props.imgSrc"/>
      </div>
      <div class="content-text">
        <h2>{{ props.head }}</h2>
        <p class="text">{{ props.text }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
p{
  margin: 0;
}
</style>