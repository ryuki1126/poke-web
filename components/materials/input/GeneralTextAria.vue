<template>
  <div class="flex items-center m-2">
    <label class="w-24" for="">{{ label }}</label>
    <textarea class="w-120 border-2 p-2 ml-4" cols="60" rows="10" :value="value"></textarea>
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
