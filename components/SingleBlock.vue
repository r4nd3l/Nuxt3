<template>
  <main>
    <ContentDoc path="/single" v-slot="{ doc }">
      <h1>{{ doc.title }}</h1>
      <h1>{{ doc.description }}</h1>
      <ContentRenderer :value="doc" />
    </ContentDoc>
  </main>
</template>

<style scoped>
main {
  border: 1px solid red;
  margin-top: 1rem;
  padding: 1rem;
}
</style>
