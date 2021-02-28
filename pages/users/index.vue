<template>
  <section>
    <h1 class="px-4">{{pageTitle}}</h1>
    <ul>
      <li v-for="user of users" :key="user.id" class="flex flex-col">
        <a href="#" @click.prevent="openShit(user)" class="py-2 px-4 text-sm text-gray-700 hover:text-gray-900"> {{ user.name }}</a>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  async fetch({store}) {
    if (store.getters['users/users'].length === 0) {
      await store.dispatch('users/fetch')
    }
  },
  data: () => ({
    pageTitle: 'Users:'
  }),
  computed: {
    users() {
      return this.$store.getters['users/users']
    }  
  },
  methods: {
    openShit(user) {
      this.$router.push('/users/' + user.id)
    }
  }
}
</script>