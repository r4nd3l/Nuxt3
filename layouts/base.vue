<template>
  <div class="base-container">
    <header>
      <slot name="header"> Content of /layouts/base.vue </slot>
    </header>
    <main>
      <p>Text above real content</p>
      <!-- Real content -->
      <slot />
      <!-- Real content -->
      <p>Text below real content</p>
    </main>
  </div>
</template>

<style>
.base-container,
header {
  border: 1px solid red;
  margin: 0.5rem;
}
</style>
