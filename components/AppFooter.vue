<template>
  <footer class="footer footer-center p-4 bg-base-300 text-base-content">
    <div>
      <ContentDoc path="/partials/footer" v-slot="{ doc }">
        <p><ContentRenderer :value="doc" /></p>
      </ContentDoc>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
div {
  content: "";
}
</style>
