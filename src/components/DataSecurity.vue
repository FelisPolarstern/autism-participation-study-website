<script setup lang="ts">
import "@/assets/textcomponents.css"
import bubbleicon from "@/assets/img/S4bubbleicons.png"

type Props = {
  lang: 'de' | 'eng',
  head: string,
  text: string,
  imgSrc: string
}
const props = defineProps<Props>()
</script>

<template>
  <div class="page">
    <h2>{{ props.head }}</h2>
    <div class="colum">
      <div> <!--- erste Spalte --->
        <img class="column-img" :src="bubbleicon"/>

      </div>
      <div>


      </div>
      <div> <!--- dritte Spalte--->

      </div>
    </div>
  </div>
</template>

<style scoped>
.colum{
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
</style>