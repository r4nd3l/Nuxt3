<script setup>
const { data: content } = await useAsyncData("about_block", () => {
  return queryContent("/about").find();
});
</script>

<template>
  <NuxtLayout>
    <section v-if="content">
      <div v-for="item in content">
        <h1>{{ item.title }}</h1>
        <h1>{{ item.description }}</h1>
        <h1>{{ item.body.children[0].children[0].value }}</h1>
        <h1>{{ item.body.children[1].children[0].value }}</h1>
      </div>
    </section>
  </NuxtLayout>
</template>

<style lang="css">
section {
  border: 1px solid red;
}
</style>
