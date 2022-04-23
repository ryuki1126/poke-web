<template>
  <div class="flex items-center">
    <label class="w-24" for="">{{ label }}</label>
    <input type="text" class="w-60 border-2 p-2 ml-4" :value="value">
  </div>
</template>

<script>
export default {
  props: {
    label: { type: String },
    value: { type: String }
  }
}
</script>
