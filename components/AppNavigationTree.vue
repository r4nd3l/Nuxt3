<script setup>
defineProps({
  navigationTree: {
    type: Array,
    default: () => [],
  },
});
</script>

<template>
  <ul class="navigation">
    <li v-for="(item, index) in navigationTree" :key="index">
      <NuxtLink :to="item._path === '/main' ? '/' : item._path">
        {{ item.title }}
      </NuxtLink>
      <!-- <AppNavigation
        v-if="item.children"
        :navigation-tree="item.children"
        class="sub-navigation"
      /> -->
    </li>
    <hr />
    <li><a href="/"> Main_href </a></li>
    <li><a href="/home"> Home_href </a></li>
    <li><a href="/about"> About_href </a></li>
  </ul>
</template>

<style scoped>
.navigation li {
  list-style-type: "";
}

.navigation ul {
  margin-left: 0.8rem;
}
</style>
