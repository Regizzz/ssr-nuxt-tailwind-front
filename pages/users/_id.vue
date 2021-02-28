<template>
  <section class="flex flex-col justify-center px-4 text-gray-700">
    <div>
      <h1 class="text-center text-xl underline">{{ user.name }}</h1>
    </div>
    
    <hr>
    <div class="flex gap-2">
      <span class="bg-purple-400 px-2">email:</span>
      <h3 class="font-mono">{{user.email}}</h3>
    </div>
  </section>
</template>

<script>
export default {
  validate( {params} ) {
    return /^\d+$/.test(params.id)
  },
  async asyncData({$axios, params}) {
    const user = await $axios.$get('https://jsonplaceholder.typicode.com/users/' + params.id)
    return {user}
  }
}
</script>