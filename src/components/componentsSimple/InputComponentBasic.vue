<template>
    <input class="c-input" v-bind="$attrs" v-model="computedValue"/>
</template>

<script>
export default {
  name: 'InputComponentBasic',
  props: {
    modelValue: {
      type:String,
      default: ''
    },
    someData:{}
  },
  computed: {
    computedValue: {
      get(){
        if (this.someData){
          return this.someData;
        }
        return this.modelValue;
      },
      set(value){
        this.$emit('update:modelvalue', value)
      }
    }
  }
}
</script>

<style scoped>
</style>
