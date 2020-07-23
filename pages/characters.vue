<template>
  <div>
    Characters live here
    <ul>
      <li v-for="char of characters" :key="char.id">
        <NuxtLink :to="char.path">{{ char.name }}</NuxtLink>
      </li>
    </ul>
    <nuxt-child />
  </div>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  async asyncData({ $content, params }) {
    const characters = await $content('characters', params.slug).fetch()
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
