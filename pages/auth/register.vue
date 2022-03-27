<template>
  <div class="hero min-h-screen bg-base-200">
    <div class="card flex-shrink-0 w-full max-w-sm shadow-2xl bg-base-100">
      <div class="card-body">
        <div class="form-control">
          <label class="label">
            <span class="label-text">name</span>
          </label>
          <input
            type="text" v-model="name" placeholder="name" class="input input-bordered">
        </div>
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
        </div>
        <div class="form-control mt-6">
          <button @click="register" class="btn btn-warning">アカウント登録</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  layout: 'home',
  data(){
    return {
      showPassword : false,
      name: '',
      email:'',
      password:''
    }
  },
  methods: {
    async register() {
      try {
        await axios.post('http://localhost:8000/api/register/', {
          data: {
            name: this.name,
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