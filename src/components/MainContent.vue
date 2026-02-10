<script setup lang="ts">
import ContentWImage from "@/components/ContentWImage.vue";
import ImageRight from "@/components/ImageRight.vue"
import {texts} from "@/components/Content";
import {images} from "@/components/Content";
import ContentFirst from "@/components/ContentFirst.vue";

const lang = "de"
const currentTexts = texts[lang] //Hole die Texte für die Sprache die in lang vorgegeben ist
const img = images["section1"].src

</script>

<template>
  <div class="page">
  <ContentFirst :lang ="lang" :head="currentTexts.section1.head" :text="currentTexts.section1.text" :imgSrc ="img" />
  <ContentWImage :lang ="lang" :head="currentTexts.section2.head" :text="currentTexts.section2.text" :imgSrc ="img" />
  </div>
</template>

<style scoped>

</style>