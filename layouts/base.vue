<template>
  <div class="base-container">
    <header>
      <slot name="navigation"> Content of /layouts/base.vue </slot>
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
