<script setup>
const route = useRoute();
const { data: navigation } = await useAsyncData("navigation", () => {
  return fetchContentNavigation();
});
</script>

<template>
  <div class="base-container">
    <header class="fixed top-0 w-full">
      <slot name="navigation">
        <AppNavigation :navigation-tree="navigation" />
      </slot>
    </header>
    <section class="bg-gray-200">
      <slot />
    </section>
    <footer>
      <AppFooter />
    </footer>
  </div>
</template>

<style lang="scss" scoped>
div {
  content: "";
}
</style>
