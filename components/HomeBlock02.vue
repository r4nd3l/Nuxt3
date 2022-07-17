<template>
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content flex-col lg:flex-row">
      <img
        src="https://placeimg.com/260/400/arch"
        class="max-w-sm rounded-lg shadow-2xl"
      />
      <div>
        <ContentDoc path="/home/block02" v-slot="{ doc }">
          <h1 class="text-5xl font-bold">{{ doc.title }}</h1>
          <p class="py-6"><ContentRenderer :value="doc" /></p>
          <button class="btn btn-primary">
            {{ doc.button }}
          </button>
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
