<template>
  <q-page class="flex flex-center">
    <h1>APP - A</h1>
    <q-btn @click="handleBtn">nav to APP - B</q-btn>
  </q-page>
</template>

<script setup>
import {useRouter} from "vue-router";

const router = useRouter()
function handleBtn () {
  if ('navigator' in window && 'serviceWorker' in navigator) {
    // Încearcă să deschidă PWA-ul App B
    window.open('https://catalinmuresian.github.io/app-b/', '_blank');
  } else {
    // Fallback la browser normal
    router.push('https://catalinmuresian.github.io/app-b/');
  }
}

</script>
