<template>
  <div>
    <Navbar />
    <main>
      <div class="container mx-auto">
        <Nuxt />
      </div>
    </main>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
export default {
  components: {
    Navbar
  }
}
</script>

<style>

</style>
