<template>
  <div>
    <header>
      <slot name="header"> Content of /layouts/base.vue </slot>
    </header>
    <main>
      <p>Text above real content</p>
      <slot />
      <p>Text below real content</p>
    </main>
  </div>
</template>
