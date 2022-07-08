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
      <hr />
      <code>Route binding => {{ route.path }}</code>
    </header>
    <main>
      <p class="header">Header block</p>
      <!-- Real content -->
      <slot />
      <!-- Real content -->
      <p class="footer">Footer block</p>
    </main>
  </div>
</template>

<style>
.base-container,
header,
.header,
.footer {
  border: 1px solid red;
  margin: 1rem 0;
  padding: 1rem;
}
</style>
