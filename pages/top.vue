<template>
  <div>
    top
  </div>
</template>

<script>
export default {
  middleware: ['auth'],
  components: {
    PokemonSuggest: () => import('~/components/materials/PokemonSuggest')
  },
  data() {
    return {
      userName: this.$auth.user.name
    }
  }
}
</script>