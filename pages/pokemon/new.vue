<template>
  <div class=" min-h-screen">
    <p>新たに育成したポケモンを登録しよう</p>
    <form>
      <div class="flex items-center">
        <label class="w-24" for="">ポケモン名</label>
        <PokemonSuggestInput class="ml-4" />
      </div>
      <GeneralInput label="ニックネーム" :value="inputValue" />
      <GeneralInput label="HP" />
      <GeneralInput label="攻撃" />
      <GeneralInput label="防御" />
      <GeneralInput label="特攻" />
      <GeneralInput label="特防" />
      <GeneralInput label="素早さ" />
      <GeneralInput label="備考" />
      <button type="submit" class="btn btn-warning px-12" @click.prevent="insertData">登録</button>
    </form>
  </div>
</template>

<script>
export default {
  components: {
    PokemonSuggestInput: () => import('~/components/materials/input/PokemonSuggestInput.vue'),
    GeneralInput: () => import('~/components/materials/input/GeneralInput.vue')
  },
  data() {
    return {
      inputValue: 'pokemon'
    }
  },
  methods: {
    insertData() {
      alert(this.inputValue)
    }
  }
}
</script>