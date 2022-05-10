<template>
  <div>
    <Navbar></Navbar>
    <Nuxt keep-alive />
  </div>
</template>
<style>
a.nuxt-link-active {
  font-weight: bold;
}
/* exact link will show the primary color for only the exact matching link */
a.nuxt-link-exact-active {
  color: #00c58e;
}
</style>
