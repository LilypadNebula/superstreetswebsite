<template>
  <div class="flex flex-col items-center text-white">
    <NuxtLink to="/" class="flex flex-col items-center w-full" exact>
      <p class="text-5xl font-comic text-main">super</p>
      <p class="text-5xl font-comic text-main">streets</p>
    </NuxtLink>
    <nav class="flex w-full text-5xl font-comic">
      <NuxtLink
        to="/characters"
        class="text-center w-1/3"
        active-class="text-alt"
        >Characters</NuxtLink
      >
      <NuxtLink to="/cast" class="text-center w-1/3" active-class="text-alt"
        >Cast</NuxtLink
      >
      <NuxtLink to="/episodes" class="text-center w-1/3" active-class="text-alt"
        >Episodes</NuxtLink
      >
    </nav>
    <div class="p-16 flex justify-center text-center text-xl">
      <Nuxt />
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import 'animate.css'
export default Vue.extend({})
</script>

<style>
@font-face {
  font-family: 'ElliotSix';
  src: url('~assets/ElliotSix.ttf');
}

@font-face {
  font-family: 'AlegreyaSans';
  src: url('~assets/AlegreyaSansSC-Regular.ttf');
}

@font-face {
  font-family: 'Montserrat';
  src: url('~assets/Montserrat-Regular.ttf');
}

body {
  height: 100vh;
  background-color: hsl(0, 0%, 20%);
}

a {
  transition: color 0.5s ease;
}

/* body {
  height: 100vh;
  background: rgb(123, 194, 214);
  background: linear-gradient(
    122deg,
    rgba(123, 194, 214, 1) 50%,
    rgba(232, 219, 236, 1) 71%,
    rgba(238, 121, 175, 1) 100%
  );
} */
</style>
