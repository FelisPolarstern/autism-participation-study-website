<script setup lang ="ts">
type Props = {
  lang: 'de' | 'eng',
  menu: any
}

const props = defineProps<Props>()
</script>

<template>
  <nav>
    <a href ="#section1">{{ props.menu.section1.text }}</a><br>
    <a href ="#section2">{{ props.menu.section2.text }}</a><br>
    <a href ="#section3">{{ props.menu.section3.text }}</a><br>
    <a href ="#section4">{{ props.menu.section4.text }}</a><br>
    <a href ="#section5">{{ props.menu.section5.text }}</a><br>
    <a href ="#section6">{{ props.menu.section6.text }}</a><br>
  </nav>
</template>

<style scoped>

</style>