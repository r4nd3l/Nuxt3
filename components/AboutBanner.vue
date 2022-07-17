<template>
  <div
    class="hero min-h-screen"
    style="background-image: url(https://placeimg.com/1000/800/arch)"
  >
    <div class="hero-overlay bg-opacity-60"></div>
    <div class="hero-content text-center text-neutral-content">
      <div class="max-w-md">
        <ContentDoc path="/about/banner" v-slot="{ doc }">
          <h1 class="mb-5 text-5xl font-bold">{{ doc.title }}</h1>
          <p class="mb-5"><ContentRenderer :value="doc" /></p>
          <button class="btn btn-primary">{{ doc.button }}</button>
        </ContentDoc>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
main {
  border: 1px solid green;

  h1:nth-child(3) {
    background: green;
  }
}
</style>
