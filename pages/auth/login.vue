<template>
  <div class="hero min-h-screen bg-base-200">
    <div class="card flex-shrink-0 w-full max-w-sm shadow-2xl bg-base-100">
      <div class="card-body">
        <div class="form-control">
          <label class="label">
            <span class="label-text">Email</span>
          </label>
          <input
            type="email" v-model="email" placeholder="email" class="input input-bordered">
        </div>
        <div class="form-control">
          <label class="label">
            <span class="label-text">Password</span>
          </label>
          <input type="password" v-model="password" placeholder="password" class="input input-bordered">
          <label class="label">
            <a href="#" class="label-text-alt link link-hover">Forgot password?</a>
          </label>
        </div>
        <div class="form-control mt-6">
          <button @click="login" class="btn btn-warning">Login</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'home',
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