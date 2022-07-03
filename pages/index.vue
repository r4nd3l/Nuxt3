<script setup>
const { data: equalQuery } = await useAsyncData("equal", () => {
  return queryContent("/about").find();
});
</script>

<template>
  <NuxtLayout>
    <ul v-if="equalQuery" style="color: black">
      <li v-for="item in equalQuery">
        <h1>{{ item.title }}</h1>
        <h1>{{ item.description }}</h1>
        <h1>{{ item.body.children[0].children[0].value }}</h1>
        <h1>{{ item.body.children[1].children[0].value }}</h1>
      </li>
    </ul>
  </NuxtLayout>
</template>
