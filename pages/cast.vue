<template>
  <div>
    IRL people live here
    <ul>
      <li v-for="member of cast" :key="member.id">
        <NuxtLink :to="member.path">{{ member.name }}</NuxtLink>
      </li>
    </ul>
    <nuxt-child />
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
