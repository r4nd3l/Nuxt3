<template>
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content flex-col lg:flex-row">
      <div class="card w-96 bg-base-100 shadow-xl">
        <div class="card-body">
          <ContentDoc path="/about/block01" v-slot="{ doc }">
            <h2 class="card-title">{{ doc.title }}</h2>
            <p><ContentRenderer :value="doc" /></p>
          </ContentDoc>
        </div>
        <figure>
          <img src="https://placeimg.com/400/225/arch" alt="Shoes" />
        </figure>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
div {
  content: "";
}
</style>
