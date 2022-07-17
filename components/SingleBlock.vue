<template>
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content text-center">
      <div class="card lg:card-side bg-base-100 shadow-xl">
        <figure>
          <img src="https://placeimg.com/400/400/arch" alt="Album" />
        </figure>
        <div class="card-body">
          <ContentDoc path="/single" v-slot="{ doc }">
            <h2 class="card-title">{{ doc.title }}</h2>
            <p>
              <ContentRenderer :value="doc" />
            </p>
            <div class="card-actions justify-end">
              <button class="btn btn-primary">{{ doc.button }}</button>
            </div>
          </ContentDoc>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
div {
  content: "";
}
</style>
