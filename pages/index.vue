<template>
  <main>
    <ContentList path="/main" v-slot="{ list }">
      <div class="blocks" v-for="main in list" :key="main._path">
        <h2>{{ main.title }}</h2>
        <p>{{ main.description }}</p>
        <ContentDoc path="/main" />
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
