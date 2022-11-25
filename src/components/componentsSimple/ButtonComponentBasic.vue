<template>
  <button v-bind="$attrs" @click="clickEvent" class="button-49">
    <slot/>
  </button>
</template>

<script>
export default {
  name: "ButtonComponentBasic",
  methods:{
    clickEvent(){
      this.$emit("clickEvent")
    }
  }
}
</script>

<style scoped>

</style>