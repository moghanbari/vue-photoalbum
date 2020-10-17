<template>
  <div>

  </div>
</template>

<script>
  import { mapGetters } from 'vuex'

  export default {
    name: 'Navbar',
    methods: {
      async logout() {
        await this.$store.dispatch('auth/logout')
        this.$router.push('/')
      }
    },
    computed: {
      ...mapGetters({
        user: 'auth/user'
      })
    }
  }
</script>

<style lang="scss" scoped>

</style>