<template>
  <div>
    top
    <p>{{ userName }}</p>
    <button @click="$auth.logout()">logout</button>
  </div>
</template>

<script>
export default {
  middleware: ['auth'],
  data() {
    return {
      userName: this.$auth.user.name
    }
  }
}
</script>