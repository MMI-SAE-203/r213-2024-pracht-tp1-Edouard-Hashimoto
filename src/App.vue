<script setup lang="ts">
import { onErrorCaptured, ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router/auto'

onErrorCaptured((err, instance, info) => {
  console.error('erreur : ', err, '\ninfo : ', info, '\ncomposant : ', instance)
  return true
})
const menuIsOpen = ref(false)

</script>

<template>
  <header>
    <button
    aria-controls="mainNav"
    aria-expanded="true"
    class="rounded-full border-2 border-red-600 bg-red-300 px-2"
    @pointerdown="menuIsOpen = !menuIsOpen">
    menu
    </button>
  <nav id="mainNav" v-show="menuIsOpen">
    <ul>
      <li><RouterLink to="/">item 1</RouterLink></li>
      <li><RouterLink to="/">item 2</RouterLink></li>
      <li><RouterLink to="/">item 3</RouterLink></li>
    </ul>
  </nav>
</header>
</template>