<script>
export default {
  created() {
    console.log("Path", this.$route.path);
    console.log("name", this.$route.name);
  },
};
</script>
<template>
  <NuxtLayout name="base">
    <HomeBanner />
    <HomeBlock01 />
    <HomeBlock02 />
  </NuxtLayout>
</template>
