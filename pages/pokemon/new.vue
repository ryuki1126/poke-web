<template>
  <div class=" min-h-screen text-center">
    <p class="text-2xl font-bold my-6">新たに育成したポケモンを登録しよう</p>
    <div class="w-1/2 mx-auto">
      <div class="grid grid-cols-2 gap-2">
        <div class="flex items-center mx-auto">
          <label class="w-24" for="">ポケモン名</label>
          <PokemonSuggestInput class="ml-4" />
        </div>
        <GeneralInput class="mx-auto" label="ニックネーム" :value="inputValue" />
        <GeneralInput class="mx-auto" label="HP" />
        <GeneralInput class="mx-auto" label="攻撃" />
        <GeneralInput class="mx-auto" label="防御" />
        <GeneralInput class="mx-auto" label="特攻" />
        <GeneralInput class="mx-auto" label="特防" />
        <GeneralInput class="mx-auto" label="素早さ" />
      </div>
      <GeneralTextAria class="mt-4" label="備考" />
      <div class="mt-4">
        <button type="submit" class="btn w-40 mx-2" @click.prevent="insertData">キャンセル</button>
        <button type="submit" class="btn btn-warning w-40 mx-2" @click.prevent="insertData">登録</button>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  components: {
    PokemonSuggestInput: () => import('~/components/materials/input/PokemonSuggestInput.vue'),
    GeneralInput: () => import('~/components/materials/input/GeneralInput.vue'),
    GeneralTextAria: () => import('~/components/materials/input/GeneralTextAria.vue')
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