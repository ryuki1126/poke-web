<template>
  <div>
    top
    <p>{{ userName }}</p>
    <button @click="$auth.logout()">logout</button>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  async fetch() {
    const res = await axios.get('http://localhost:8000/api/test')
    console.log(res)
  },
  data() {
    return {
      userName: this.$auth.user.name
    }
  }
  
}
</script>