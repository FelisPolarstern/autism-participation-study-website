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
    <h2>{{ props.head }}</h2>
    <p class="text">{{ props.text }}</p>
    </div>
  <!--</div>--->
</template>

<style scoped>
h2 {
  margin-bottom: 0;
}
text {
  margin-top: 0;
}
p{
  margin-top: 0;
}

</style>