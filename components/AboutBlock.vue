<template>
  <main>
    <ContentList path="/about" v-slot="{ list }">
      <div class="blocks" v-for="about in list" :key="about._path">
        <h2>{{ about.title }}</h2>
        <p>{{ about.description }}</p>

        <div v-for="content in about.body.children">
          <p>{{ content.children[0].value }}</p>
        </div>
      </div>
    </ContentList>
  </main>
</template>

<style scoped>
.blocks {
  border: 1px solid red;
  margin: 1rem 0;
  padding: 1rem;
}
</style>
