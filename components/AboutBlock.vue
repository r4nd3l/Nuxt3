<template>
  <main>
    <ContentList path="/about" v-slot="{ list }">
      <div class="blocks" v-for="about in list" :key="about._path">
        <h2>{{ about.title }}</h2>
        <p>{{ about.description }}</p>

        <hr />
        <pre>{{ about.body.children }}</pre>
        <hr />

        <div v-for="(content, index) in about.body.children">
          <b>{{ index }}</b>
          <pre class="contentBody">{{ content.children[0].value }}</pre>
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
.contentBody {
  border: 10px solid green;
  padding: 1rem;
}
</style>
