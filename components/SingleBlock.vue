<template>
  <main>
    <ContentDoc path="/single" v-slot="{ doc }">
      <h1>{{ doc.title }}</h1>
      <h1>{{ doc.description }}</h1>
      <h1>{{ doc.note }}</h1>
      <ContentRenderer :value="doc" />
    </ContentDoc>
    <div class="p-4">
      <span class="material-icons-outlined"> home </span>
      <span class="material-icons">pie_chart</span>
      <!-- Filled -->
      <span class="material-icons-outlined">pie_chart</span>
      <!-- Outlined -->
      <span class="material-icons-round">pie_chart</span>
      <!-- Round -->
      <span class="material-icons-sharp">pie_chart</span>
      <!-- Sharp -->
      <span class="material-icons-two-tone">pie_chart</span>
      <!-- Two Tone -->
    </div>
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
