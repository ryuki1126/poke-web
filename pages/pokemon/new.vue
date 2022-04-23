<template>
  <div class=" min-h-screen">
    <p>新たに育成したポケモンを登録しよう</p>
    <form>
      <div class="flex items-center">
        <label class="w-24" for="">ポケモン名</label>
        <PokemonSuggestInput class="ml-4" />
      </div>
      <GeneralInput />
    </form>
  </div>
</template>

<script>
export default {
  components: {
    PokemonSuggestInput: () => import('~/components/materials/input/PokemonSuggestInput.vue'),
    GeneralInput: () => import('~/components/materials/input/GeneralInput.vue')
  },
}
</script>