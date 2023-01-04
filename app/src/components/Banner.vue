<script setup lang="ts">
const menuItems: { title: string, path: string }[] = [
  {
    title: "Products",
    path: "/"
  },
  {
    title: "Cart",
    path: "/cart"
  }
]
</script>

<template>
  <v-app-bar>
    <v-toolbar-title class="title">
      <RouterLink to="/">CESI Eats</RouterLink>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items>
      <v-btn v-for="item in menuItems" :key="item.title" :to="item.path">
        {{ item.title }}
      </v-btn>
    </v-toolbar-items>
  </v-app-bar>
</template>

<style scoped>
</style>
