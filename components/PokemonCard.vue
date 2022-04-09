<template>
  <div class="w-2/5 h-52 m-2 card bg-white shadow-xl">
    <div class="mx-4 mt-6 flex justify-between">
      <p class="text-2xl font-bold"><nuxt-link to="/mypage">アタッカーピカチュウ</nuxt-link></p>
      <p>投稿日 : 2022/3/14 10:20</p>
    </div>
    <div>
      <div class="flex">
        <img class="w-32 h-32 m-4 rounded-lg" src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/official-artwork/25.png" alt="movie">
        <div class="w-full mt-4 mr-4">
          <p class="text-lg">ポケモン名：ピカチュウ</p>
          <div class="mt-2 flex">
            <p>調整：</p>
            <p class="mr-1">H:0</p>
            <p class="mr-1 text-blue-500" >A:0</p>
            <p class="mr-1">B:0</p>
            <p class="mr-1">C:252</p>
            <p class="mr-1">D:4</p>
            <p class="text-red-500">S:252</p>
          </div>
          <div class="mt-2">
            <p class=" text-gray-400 ">text here</p>
          </div>
          <div class="flex justify-end">
            <p>good:<span>12</span></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>