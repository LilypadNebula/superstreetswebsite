<template>
  <div>
    <p class="text-3xl">{{ cast.name }}</p>
    <p class="text-2xl">@{{ cast.twitter }}</p>
    <p class="text-2xl">{{ cast.pronouns }}</p>
    <nuxt-content :document="cast" />
  </div>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  async asyncData({ $content, params }) {
    const cast = await $content('cast', params.slug).fetch()

    return { cast }
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
