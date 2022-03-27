<template>
  <div class="hero min-h-screen bg-base-200">
  <div class="hero-content text-center">
    <div class="max-w-md">
      <h1 class="text-5xl font-bold">ポケモン努力値管理</h1>
      <p class="py-6">育てたポケモンの努力値配分を記録して<br>自分のポケモンを管理しよう！</p>
      <nuxt-link to="/auth/register" class="w-36 btn btn-warning mx-2">アカウント登録</nuxt-link>
      <nuxt-link to="/auth/login" class="w-36 btn btn-warning mx-2">ログイン</nuxt-link>
    </div>
  </div>
</div>
</template>

<script>
import axios from 'axios'
export default {
  layout: 'home',
  async fetch() {
    const res = await axios.get('http://localhost:8000/api/test')
    console.log(res)
  },
}
</script>
