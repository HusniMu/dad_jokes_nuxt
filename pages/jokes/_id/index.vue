<template lang="">
  <div>
    <div class="flex justify-center w-full mt-3">
      <div class="block p-6 rounded-lg shadow-lg bg-white">
        <h5 class="text-gray-900 text-xl leading-tight font-medium mb-2">
          Joke Id: {{ $route.params.id }}
        </h5>
        <p class="text-gray-700 text-base mb-4">
          {{ joke }}
        </p>
        <NuxtLink
          :to="{ name: 'jokes' }"
          class="bg-gray-300 hover:bg-gray-600 hover:text-white px-3 py-1 rounded"
        >
          Back
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  head() {
    return {
      title: this.joke,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for corny dad jokes',
        },
      ],
    }
  },
  data() {
    return {
      joke: null,
    }
  },
  async created() {
    const config = {
      headers: {
        Accept: 'application/json',
      },
    }
    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config,
      )
      this.joke = res.data.joke
      console.log(this.joke)
    } catch (err) {
      console.log(err)
    }
  },
}
</script>
<style lang=""></style>
