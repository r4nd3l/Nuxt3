<script setup>
const { data: content } = await useAsyncData("footer", () => {
  return queryContent("/_partials/footer").where({ _partial: true }).find();
});
</script>

<template>
  <footer
    class="footer footer-center p-4 bg-base-300 text-base-content"
    v-if="content"
  >
    <div v-for="item in content">
      <h1>{{ item.title }} - {{ item.body.children[0].children[0].value }}</h1>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
div {
  content: "";
}
</style>
