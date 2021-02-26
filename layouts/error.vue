<template>
  <div class="h-screen w-screen flex flex-col justify-center content-center flex-wrap text-purple-600">
    <p class="error-text">404</p>
    <nuxt-link to="/" class="text-center">Home</nuxt-link>
  </div>
</template>

<style scoped>
.error-text {
      font-size: 130px;
    }

@media (min-width: 768px) {
  .error-text {
    font-size: 220px;
  }
}
</style>