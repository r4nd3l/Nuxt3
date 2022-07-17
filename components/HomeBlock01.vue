<template>
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content flex-col lg:flex-row-reverse">
      <ContentDoc path="/home/block01" v-slot="{ doc }">
        <div class="text-center lg:text-left">
          <h1 class="text-5xl font-bold">{{ doc.title }}</h1>
          <p class="py-6">
            <ContentRenderer :value="doc" />
          </p>
        </div>
        <div class="card flex-shrink-0 w-full max-w-sm shadow-2xl bg-base-100">
          <div class="card-body">
            <div class="form-control">
              <label class="label">
                <span class="label-text">Email</span>
              </label>
              <input
                type="text"
                placeholder="email"
                class="input input-bordered"
              />
            </div>
            <div class="form-control">
              <label class="label">
                <span class="label-text">Password</span>
              </label>
              <input
                type="text"
                placeholder="password"
                class="input input-bordered"
              />
              <label class="label">
                <a href="#" class="label-text-alt link link-hover"
                  >Forgot password?</a
                >
              </label>
            </div>
            <div class="form-control mt-6">
              <button class="btn btn-primary">{{ doc.button }}</button>
            </div>
          </div>
        </div>
      </ContentDoc>
    </div>
  </div>
</template>

<style lang="scss" scoped>
div {
  content: "";
}
</style>
