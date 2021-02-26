<template>
  <div class="h-screen flex justify-center items-center">
    <form class="w-full max-w-xs bg-purple-400 flex flex-col py-5 px-8 rounded-lg shadow-lg" action="">
      <label class="text-gray-900 font-bold py-2" for="">Username</label>
      <input class="text-gray-900 shadow border rounded border-gray-300 focus:outline-none focus:shadow-outline py-1 px-3 mb-3" type="text" placeholder="Username">
      <label class="text-gray-900 font-bold py-2" for="">Password</label>
      <input class="text-gray-900 shadow border rounded border-gray-300 mb-3 py-1 px-3 focus:outline-none focus:shadow-outline" type="password" placeholder="********">
      <div class="flex justify-between items-center my-4">
        <button class="bg-purple-700 hover:bg-blue-700 text-white font-bold rounded py-2 px-4">
          Sign In
        </button>
        <a class="text-gray-700 hover:text-gray-900 font-bold" href="#">
          Forgot Password?
        </a>
        
      </div>
      <nuxt-link to="/" class="text-gray-900 text-xs">Home</nuxt-link>
    </form>
  </div>
</template>

<script>
export default {
  layout: 'empty'
}
</script>