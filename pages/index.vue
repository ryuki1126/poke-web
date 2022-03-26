<template>
  <Tutorial/>
</template>

<script>
import axios from 'axios'
export default {
  async fetch() {
      const res = await axios.get('http://localhost:8000/api/test')
      console.log(res)
    },
}
</script>
