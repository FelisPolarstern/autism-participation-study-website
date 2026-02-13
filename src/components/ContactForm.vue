<script setup lang="ts">
import { computed } from 'vue'

type Props = {
  lang: 'de' | 'eng'
  head: string
  text: string
}

const props = defineProps<Props>()

const buttonText = computed(() =>
    props.lang === 'eng' ? 'Send mail' : 'Mail senden'
)

const subjectText = computed(() =>
    props.lang === 'eng' ? 'Contact request' : 'Kontaktanfrage'
)

const bodyText = computed(() =>
    props.lang === 'eng'
        ? "Hi, I'm interested in taking part in the interview."
        : 'Hallo, ich bin bereit, am Interview teilzunehmen.'
)

function submitForm() {
  const to = 'nadja.just@informatik.tu-chemnitz.de'
  const subject = encodeURIComponent(subjectText.value)
  const body = encodeURIComponent(bodyText.value)
  window.location.href = `mailto:${to}?subject=${subject}&body=${body}`
}
</script>

<template>
  <div class="content">
    <h2>{{ props.head }}</h2>
    <p class="text">{{ props.text }}</p>

    <form @submit.prevent="submitForm">
      <button type="submit" class="btn">
        {{ buttonText }}
      </button>
    </form>
  </div>
</template>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

h2 {
  margin: 0 0 0.05em 0;
}

p {
  margin: 0;
}

.btn {
  width: 30%;
  min-height: 3rem;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0;
  line-height: 1;

  border: none;
  border-radius: 6px;
  background: #0A4152;
  color: #fff;
  cursor: pointer;
  transition: background-color 150ms ease-in-out;
  font-size: 1.5em;
  font-family: 'Bebas Neue', cursive;
  font-weight: 700;
  margin-top: 1em;
}

.btn:hover {
  background: #F6724B;
}
</style>