<template>
  <main>
    <ContentList path="/home" v-slot="{ list }">
      <div class="blocks" v-for="home in list" :key="home._path">
        <h2>{{ home.title }}</h2>
        <p>{{ home.description }}</p>
        <ContentDoc path="/home" />
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
