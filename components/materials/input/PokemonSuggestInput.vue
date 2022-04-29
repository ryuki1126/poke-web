<template>
  <div>
    <vue-simple-suggest
      class="w-60 m-2"
      v-model="selected"
      :list="japanesePokemonNames"
      :filter-by-query="true">
    </vue-simple-suggest>
  </div>

</template>

<script>
import VueSimpleSuggest from 'vue-simple-suggest'
import 'vue-simple-suggest/dist/styles.css'
import pokemonList from "@/assets/json/japanesePokemonNames.json"
export default {
  components: {
    VueSimpleSuggest
  },
  data() {
    return {
      selected: null,
      items: ["Anton", "Andrey", "Sasha", "Vladimir", "Dima"],
      japanesePokemonNames: []
    }
  },
  mounted() {
    pokemonList.forEach(element => {
      const pokemonName = element['name_ja']
      this.japanesePokemonNames.push(pokemonName)
    })
  }
}
</script>