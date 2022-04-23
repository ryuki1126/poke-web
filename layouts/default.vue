<template>
  <div>
    <div class="navbar bg-warning">
      <div class="flex-1">
        <nuxt-link to="/top" class="btn btn-ghost normal-case text-xl">ポケモン努力値管理</nuxt-link>
      </div>
      <!-- TODO: ゲストでログインでログインする場合はアカウント登録ボタンを作成を替わりに表示させる -->
      <div class="flex-none gap-2">
        <div class="dropdown dropdown-end">
          <label tabindex="0" class="btn btn-ghost btn-circle avatar mr-4">
            <div class="w-10 rounded-full">
              <img src="https://api.lorem.space/image/face?hash=33791" />
            </div>
          </label>
          <ul tabindex="0" class="mt-3 p-2 shadow menu menu-compact dropdown-content bg-base-100 rounded-box w-52">
            <li><nuxt-link to="/pokemon/new">育成ポケモン登録</nuxt-link></li>
            <li><nuxt-link to="/mypage">マイページ</nuxt-link></li>
            <li><nuxt-link to="/config">設定</nuxt-link></li>
            <li><button @click="$auth.logout()">ログアウト</button></li>
          </ul>
        </div>
      </div>
    </div>
    <div>
      <Nuxt />
    </div>
    <footer class="footer footer-center p-4 bg-base-300 text-base-content">
      <div>
        <p>Copyright © {{ new Date().getFullYear() }} - All right reserved by ACME Industries Ltd</p>
      </div>
    </footer>
  </div>
</template>