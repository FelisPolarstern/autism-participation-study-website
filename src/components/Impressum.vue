<script setup lang="ts">
import {computed} from 'vue'

type Props = {
  lang: 'de' | 'eng'
}
const props = defineProps<Props>()

const titleText = computed(() =>
  props.lang === 'de' ? 'Impressum' : 'Imprint'
)
</script>

<template>
  <div class="footer">
  <div class="page imprint">
  <h3 v-html="titleText"></h3>
  <p class="text textImprint">
    Nadja Just <br>
    Straße der Nationen 62, 09111 Chemnitz<br>
    0371 531-35852 <br>
    nadja.just@informatik.tu-chemnitz.de <br>
  </p>
  </div>
  </div>
</template>

<style scoped>
h3 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 2rem;
  font-weight: 400;
  color: white;
  margin-bottom: 0rem;
  margin-top: 0.5rem;
}
.imprint {
  display: block;
  padding-top: 1rem;
  padding-bottom: 1rem;
}

.textImprint{
  color: white;
  font-size: 1rem;
  margin-bottom: 0rem;
  margin-top: 0.5rem;
}
.hr-border{
  height: 2px;
  color: #F6724B;
}
.footer{
  background-color: #F6724B;
}
</style>