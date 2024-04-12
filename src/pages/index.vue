<script setup lang="ts" >
import { ref } from 'vue'
const sectionOpen = ref(1)
const sectionsData = [
    {
      label: 'bouton 1',
      texte: `texte panneau 1 Lorem ipsum dolor sit ame
      consectetur adipisicing elit. Inventore animi dolore,
      rerum magni laudantium quod excepturi laboriosam, 
      ex modi debitis harum reprehenderit eaque quam ut
      ea molestiae. Id, cum dolor!`
    },
    {
      label: 'bouton 2',
      texte: `texte panneau 2 Amet alias provident quos quis, 
      Officia ut ab dolores quos dolorem accusamus ad,
      consectetur unde minima, ipsum eligendi inventore id
      labore, laborum rerum laboriosam corrupti iste.
      Distinctio, perspiciatis!`
    },
    {
      label: 'bouton 3',
      texte: `texte panneau 3 Repudiandae corporis voluptates, 
      odit reprehenderit sint pariatur at voluptatum, cumque
      quia sit eligendi ex culpa eos, alias magnam molestiae
      id modi accusantium ipsa eveniet accusamus. Tempora 
      quis corporis et nam.`
    }
  ]
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
<section v-for="({ label, texte }, key) of sectionsData" :v-key="key">
  <pre class="font-mono">key : {{ key }}</pre>
  <pre class="font-mono">label : {{ label }}</pre>
  <pre class="font-mono">texte : {{ texte }}</pre>
</section>
</template>
