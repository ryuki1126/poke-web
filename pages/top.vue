<template>
  <div>
    <div class="flex items-center flex-col my-4">
      <div class="w-2/5 h-40 my-2 card card-side bg-base-100 shadow-xl">
        <figure><img src="https://api.lorem.space/image/movie?w=200&h=280" alt="Movie"></figure>
        <div class="card-body">
          <h2 class="card-title">New movie is released!</h2>
          <p>Click the button to watch on Jetflix app.</p>
          <div class="card-actions justify-end">
            <button class="btn btn-warning">Watch</button>
          </div>
        </div>
      </div>
      <div class="w-2/5 h-40 my-2 card card-side bg-base-100 shadow-xl">
        <figure><img src="https://api.lorem.space/image/movie?w=200&h=280" alt="Movie"></figure>
        <div class="card-body">
          <h2 class="card-title">New movie is released!</h2>
          <p>Click the button to watch on Jetflix app.</p>
          <div class="card-actions justify-end">
            <button class="btn btn-warning">Watch</button>
          </div>
        </div>
      </div>
      <div class="w-2/5 h-40 my-2 card card-side bg-base-100 shadow-xl">
        <figure><img src="https://api.lorem.space/image/movie?w=200&h=280" alt="Movie"></figure>
        <div class="card-body">
          <h2 class="card-title">New movie is released!</h2>
          <p>Click the button to watch on Jetflix app.</p>
          <div class="card-actions justify-end">
            <button class="btn btn-warning">Watch</button>
          </div>
        </div>
      </div>
      <div class="w-2/5 h-40 my-2 card card-side bg-base-100 shadow-xl">
        <figure><img src="https://api.lorem.space/image/movie?w=200&h=280" alt="Movie"></figure>
        <div class="card-body">
          <h2 class="card-title">New movie is released!</h2>
          <p>Click the button to watch on Jetflix app.</p>
          <div class="card-actions justify-end">
            <button class="btn btn-warning">Watch</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  middleware: ['auth'],
  components: {
    PokemonSuggest: () => import('~/components/materials/PokemonSuggest')
  },
  data() {
    return {
      userName: this.$auth.user.name
    }
  }
}
</script>