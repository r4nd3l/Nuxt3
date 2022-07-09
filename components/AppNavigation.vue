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
    </li>
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
