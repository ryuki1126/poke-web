<template>
  <PokemonCard />
</template>

<script>
export default {
  components: {
    PokemonCard: () => import('~/components/PokemonCard.vue')
  },
}
</script>
