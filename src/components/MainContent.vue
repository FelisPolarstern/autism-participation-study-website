<script setup lang="ts">
import { computed } from 'vue'
import {texts} from "@/components/Content";
import ContentTextOnly from "@/components/ContentTextOnly.vue";
import SideNav from "@/components/SideNav.vue";
import ContactForm from "@/components/ContactForm.vue";
import {menu} from "@/components/Content";
import {title} from "@/components/Content"
type Props = {
  lang: 'de' | 'eng'
}

const props = defineProps<Props>()
const currentTexts = computed(() => texts[props.lang]) // reaktiv bei Sprachwechsel
const menuTexts = computed(() => menu[props.lang])
const titleTexts = computed(() => title[props.lang])

</script>

<template>
  <div class="page">
    <div class="sidenav">
      <SideNav :lang="props.lang" :menu="menuTexts"/>
    </div>
    <div class="content">
      <section id="section1">
        <ContentTextOnly :lang="props.lang" :head="currentTexts.section1.head" :text="currentTexts.section1.text"/>
      </section>
      <section id="section2">
        <ContentTextOnly :lang="props.lang" :head="currentTexts.section2.head" :text="currentTexts.section2.text"/>
      </section>
      <section id="section3">
        <ContentTextOnly :lang="props.lang" :head="currentTexts.section3.head" :text="currentTexts.section3.text"/>
      </section>
      <section id="section4">
        <ContentTextOnly :lang="props.lang" :head="currentTexts.section4.head" :text="currentTexts.section4.text"/>
      </section>
      <section id="section5">
        <ContentTextOnly :lang="props.lang" :head="currentTexts.section5.head" :text="currentTexts.section5.text" />
      </section>
      <section id="section6">
        <ContactForm :lang="props.lang" :head="currentTexts.section6.head" :text="currentTexts.section6.text"/>
      </section>
    </div>
  </div>
</template>

<style scoped>

</style>