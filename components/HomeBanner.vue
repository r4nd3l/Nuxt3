<template>
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content text-center">
      <div class="max-w-md">
        <ContentDoc path="/home/banner" v-slot="{ doc }">
          <h1 class="text-5xl font-bold">{{ doc.title }}</h1>
          <p class="py-6">
            <ContentRenderer :value="doc" />
          </p>
          <button class="btn btn-primary">{{ doc.button }}</button>
        </ContentDoc>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
div {
  content: "";
}
</style>
