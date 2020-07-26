<template>
  <div class="flex justify-between">
    <div class="w-1/4 text-center">
      <p class="text-3xl">{{ character.name }}</p>
      <p class="text-2xl">{{ character.playbook }}</p>
    </div>
    <div class="w-1/2 text-justify">
      <nuxt-content :document="character" />
    </div>
  </div>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  async asyncData({ $content, params }) {
    const character = await $content('characters', params.slug).fetch()

    return { character }
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
