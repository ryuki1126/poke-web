<template>
  <div>
    login
    <div>
      <input
        type="email"
        v-model="email"
        placeholder="email"
        class="input input-bordered input-warning w-full max-w-xs"
      >
      <input
        :type="showPassword ? 'text' : 'password'"
        v-model="password"
        placeholder="password"
        class="input input-bordered input-warning w-full max-w-xs"
      >
      <button
        @click="login"
        class="btn btn-outline btn-warning"
      >
        login
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      showPassword : false,
      email:'',
      password:''
    }
  },
  methods: {
    async login() {
      try {
        await this.$auth.loginWith('local', {
          data: {
            email: this.email,
            password: this.password
          }
        })
      } catch (err) {
        console.log(`error: ${err}`)
      }
    }
  }
}
</script>