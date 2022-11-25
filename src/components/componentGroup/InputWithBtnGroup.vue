<template>
  <div class="inner-wrap">
    <slot>
    <input-component-basic v-bind="$attrs"/>
    </slot>
    <button-component-basic @clickEvent="clickEvent">
      <slot>{{btnName}}</slot>
    </button-component-basic>
  </div>
</template>

<script>
import InputComponentBasic from '@/components/componentsSimple/InputComponentBasic'
import ButtonComponentBasic from "@/components/componentsSimple/ButtonComponentBasic";

export default {
  name: "InputWithBtnGroup",
  props:{
    btnName:String
  },
  components: {
    ButtonComponentBasic,
    InputComponentBasic
  },
  methods:{
    clickEvent(){
      alert('Метод вызванный')
    }
  }
}
</script>

<style scoped>
</style>