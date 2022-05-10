<template lang="">
  <div>
    <h1>About Page</h1>
    <p>This app display list of dad jokes</p>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: 'About',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for corny dad jokes',
        },
      ],
    }
  },
}
</script>
<style lang=""></style>
