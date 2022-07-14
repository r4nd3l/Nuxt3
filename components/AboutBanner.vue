<template>
  <main>
    <ContentDoc path="/about/banner" v-slot="{ doc }">
      <h1>{{ doc.title }}</h1>
      <h1>{{ doc.description }}</h1>
      <h1>{{ doc.note }}</h1>
      <ContentRenderer :value="doc" />
    </ContentDoc>
  </main>
</template>

<style lang="scss" scoped>
main {
  border: 1px solid green;

  h1:nth-child(3) {
    background: green;
  }
}
</style>
