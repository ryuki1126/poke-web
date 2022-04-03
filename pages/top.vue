<template>
  <div>
    <PokemonCard />
    <PokemonCard />
    <PokemonCard />
    <PokemonCard />
  </div>
</template>

<script>
export default {
  middleware: ['auth'],
  components: {
    PokemonCard: () => import('~/components/PokemonCard')
  },
  data() {
    return {
      userName: this.$auth.user.name
    }
  }
}
</script>