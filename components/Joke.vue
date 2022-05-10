<template lang="">
  <div class="flex justify-center w-full mt-3">
    <div class="block p-6 rounded-lg shadow-lg bg-white">
      <h5 class="text-gray-900 text-xl leading-tight font-medium mb-2">
        ---
      </h5>
      <p class="text-gray-700 text-base mb-4">
        {{ joke }}
      </p>
      <NuxtLink
        :to="{ name: 'jokes-id', params: { id: id } }"
        type="button"
        class="inline-block px-6 py-2.5 bg-blue-600 text-white font-medium text-xs leading-tight uppercase rounded shadow-md hover:bg-blue-700 hover:shadow-lg focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-blue-800 active:shadow-lg transition duration-150 ease-in-out"
      >
        Detail
      </NuxtLink>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Joke',
  props: ['joke', 'id'],
}
</script>
<style lang=""></style>
