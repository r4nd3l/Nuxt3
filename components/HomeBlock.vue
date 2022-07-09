<script setup>
const { data: content } = await useAsyncData("home", () => {
  return queryContent("/home").find();
});
</script>

<template v-if="content">
  <section v-for="item in content">
    <div>
      <h1>{{ item.title }}</h1>
      <h1>{{ item.description }}</h1>
      <h1>{{ item.body.children[0].children[0].value }}</h1>
      <!-- <h1>{{ item.body.children[1].children[0].value }}</h1> -->
    </div>
  </section>
  <div>omeBlock</div>
</template>

<style scoped>
section {
  border: 1px solid red;
  margin-top: 1rem;
  padding: 1rem;
}
</style>
