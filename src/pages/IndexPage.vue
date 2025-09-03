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
  router.push('https://catalinmuresian.github.io/app-b/')
}

</script>
