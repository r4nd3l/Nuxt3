<template>
  <main>
    <ContentList path="/about" v-slot="{ list }">
      <div class="blocks" v-for="about in list" :key="about._path">
        <h2>{{ about.title }}</h2>
        <p>{{ about.description }}</p>
        <ContentDoc path="/about" />
      </div>
    </ContentList>
  </main>
</template>

<style>
.blocks {
  border: 1px solid red;
  margin: 1rem 0;
  padding: 1rem;
}
</style>
