<template>
  <div class="flex flex-col items-center">
    <NuxtLink to="/" class="flex flex-col items-center">
      <p class="text-5xl font-comic text-main">super</p>
      <p class="text-5xl font-comic text-main">streets</p>
    </NuxtLink>
    <nav class="flex justify-around w-full text-3xl">
      <NuxtLink to="/characters">Characters</NuxtLink>
      <NuxtLink to="/cast">Cast</NuxtLink>
      <NuxtLink to="/episodes">Episodes</NuxtLink>
    </nav>
    <Nuxt />
  </div>
</template>

<script>
import Vue from 'vue'
export default Vue.extend({})
</script>

<style>
@font-face {
  font-family: 'ElliotSix';
  src: url('~assets/ElliotSix.ttf');
}
</style>
