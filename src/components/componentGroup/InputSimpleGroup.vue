<template>
  <div class="inner-wrap">
    <div class="label-wrap">
    <label-component-basic v-if="label" :for="id">
      <slot name="label">{{label}}</slot>
    </label-component-basic>
    <slot>
      <input-component-basic :id="id" v-bind="$attrs"/>
    </slot>
    </div>
  </div>
</template>

<script>
import LabelComponentBasic from '../componentsSimple/LabelComponentBasic'
import InputComponentBasic from '../componentsSimple/InputComponentBasic'

export default {
  name: "InputSimpleGroup",
  components:{
    LabelComponentBasic,
    InputComponentBasic
  },
  props: {
    label: {
      type: String,
      default: ''
    },
    id: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped>
  .label-wrap{
    display: flex;
    flex-direction: column;
  }
</style>