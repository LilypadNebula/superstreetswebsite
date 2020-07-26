<template>
  <div class="flex flex-col items-center w-full">
    Characters live here
    <ul>
      <li v-for="char of characters" :key="char.id">
        <NuxtLink :to="char.path">{{ char.name }}</NuxtLink>
      </li>
    </ul>
    <nuxt-child :key="$route.params.slug" />
  </div>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  async asyncData({ $content, params }) {
    const characters = await $content('characters').fetch()
    return { characters }
  },
})
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>
