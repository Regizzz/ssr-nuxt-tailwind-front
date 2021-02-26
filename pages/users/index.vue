<template>
  <section>
    <h1 class="px-4">Users:</h1>
    <ul>
      <li v-for="user of users" :key="user.id" class="flex flex-col">
        <a href="#" @click.prevent="openShit(user)" class="py-2 px-4 text-sm text-gray-700 hover:text-gray-900"> {{ user.name }}</a>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  async asyncData( {$axios} ) {
    const users = await $axios.$get('https://jsonplaceholder.typicode.com/users')
    return { users }
  },
  data: () => ({
    users: []
  }),
  methods: {
    openShit(user) {
      this.$router.push('/users/' + user.id)
    }
  }
}
</script>