<script setup lang="ts" >
import { ref } from 'vue'
const sectionOpen = ref(1)
</script>

<template>
  <h1 class="text-2xl">Bonjour tout le monde !</h1>
  <section>
  <btn class="text-xl" @pointerdown="sectionOpen = 1">bouton 1</btn>
  <p v-show="sectionOpen === 1">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
</section>
<section>
  <btn class="text-xl" @pointerdown="sectionOpen = 2">bouton 2</btn>
  <p v-show="sectionOpen === 2">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
</section>
<section>
  <btn class="text-xl" @pointerdown="sectionOpen = 3">bouton 3</btn>
  <p v-show="sectionOpen === 3">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
</section>
</template>
