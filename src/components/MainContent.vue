<script setup lang="ts">
import ContentWImage from "@/components/ContentWImage.vue";
import {texts} from "@/components/Content";
import {images} from "@/components/Content";
import ContentFirst from "@/components/ContentFirst.vue";
import DataSecurity from "@/components/DataSecurity.vue";
import SideNav from "@/components/SideNav.vue";

const lang = "de"
const currentTexts = texts[lang] //Hole die Texte für die Sprache die in lang vorgegeben ist
const img = images["section1"].src

</script>

<template>
  <div class="page">
    <div class="side-nav">
      <SideNav />
    </div>
    <div class="content">
      <section id="section1">
        <ContentFirst :lang="lang" :head="currentTexts.section1.head" :text="currentTexts.section1.text" :imgSrc="img"/>
      </section>
      <section id="section2">
        <ContentWImage :lang="lang" :head="currentTexts.section2.head" :text="currentTexts.section2.text" :imgSrc="img"/>
      </section>
      <section id="section3">
        <DataSecurity :lang="lang" :head="currentTexts.section3.head" :text="currentTexts.section3.text" :imgSrc="img"/>
      </section>
      <section id="section4">
        <ContentWImage :lang="lang" :head="currentTexts.section4.head" :text="currentTexts.section4.text" :imgSrc="img"/>
      </section>
      <section id="section5">
        <ContentWImage :lang="lang" :head="currentTexts.section5.head" :text="currentTexts.section5.text" :imgSrc="img"/>
      </section>
      <section id="section6">
        <ContentWImage :lang="lang" :head="currentTexts.section6.head" :text="currentTexts.section6.text" :imgSrc="img"/>
      </section>
    </div>


  </div>
</template>

<style scoped>
.page {
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  align-items: flex-start;
}

.side-nav {
  flex: 0 0 20%;
  margin: 1em;
  position: sticky;
  top: 1em;
  align-self: flex-start;
}
.content {
  flex: 1;
}
</style>