<template lang="">
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="text" placeholder="Search" />
    <input type="submit" value="Serch Jokes" />
  </form>
</template>
<script>
export default {
  name: 'Search',
  data() {
    return {
      text: '',
    }
  },
  methods: {
    onSubmit() {
      this.$emit('search-text', this.text)
      // this.text = ''
    },
  },
}
</script>
<style lang=""></style>
