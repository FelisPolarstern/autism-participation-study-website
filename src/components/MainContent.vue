<script setup lang="ts">
import ImageLeft from "@/components/ImageLeft.vue";
import ImageRight from "@/components/ImageRight.vue"
import {texts} from "@/components/Content";
import {images} from "@/components/Content";

const lang = "de"
const currentTexts = texts[lang] //Hole die Texte für die Sprache die in lang vorgegeben ist
const img = images["section1"].src

</script>

<template>
  <ImageLeft :lang ="lang" :head="currentTexts.section1.head" :text="currentTexts.section1.text" :imgSrc ="img" />
</template>

<style scoped>

</style>