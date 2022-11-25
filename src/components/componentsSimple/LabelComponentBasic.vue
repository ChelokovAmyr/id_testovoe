<template>
  <label v-bind="$attrs">
    <slot/>
  </label>
</template>

<script>
export default {
  name: "LabelComponentBasic"
}
</script>

<style scoped>

</style>