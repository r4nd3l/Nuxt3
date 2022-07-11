<script setup>
const route = useRoute();
const { data: navigation } = await useAsyncData("navigation", () => {
  return fetchContentNavigation();
});
</script>

<template>
  <div class="base-container">
    <header>
      <slot name="navigation">
        <AppNavigation :navigation-tree="navigation" />
      </slot>
    </header>
    <section class="bg-gray-200">
      <p class="header">Header block</p>
      <!-- Real content -->
      <slot />
      <!-- Real content -->
      <p class="footer">Footer block</p>
    </section>
  </div>
</template>

<style lang="scss" scoped>
.base-container,
header,
section {
  border: 1px solid blue;
  margin: 1rem;

  p {
    border: 1px solid red;
    margin: 1rem 0;
    padding: 1rem 0;
  }

  slot {
    border: 1px solid green;
  }
}
</style>
