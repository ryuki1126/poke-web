<template>
  <div>
    <dir>
      <p class="text-2xl font-bold text-center">新着ポケモン一覧</p>
      <div class="my-4 flex flex-wrap justify-center">
        <PokemonCard />
        <PokemonCard />
        <PokemonCard />
        <PokemonCard />
        <PokemonCard />
        <PokemonCard />
        <PokemonCard />
        <PokemonCard />
      </div>
    </dir>
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