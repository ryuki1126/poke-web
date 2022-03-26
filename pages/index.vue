<template>
  <div>
    hello
    <PokemonSuggest />
  </div>
</template>

<script>
import axios from 'axios'
export default {
  components: {
    PokemonSuggest: () => import('~/components/materials/PokemonSuggest'),
  },
  async fetch() {
    const res = await axios.get('http://localhost:8000/api/test')
    console.log(res)
  },
}
</script>
