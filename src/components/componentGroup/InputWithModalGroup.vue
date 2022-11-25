<template>
  <div class="inner-wrap">
    <modal-component-basic :opened="opened" :listName="listName" @sendList="sendList">
      <slot>
      </slot>
    </modal-component-basic>
    <input-component-basic v-bind="$attrs" :someData="someData"/>
    <button-component-basic @clickEvent="clickEvent">
      <slot>{{btnName}}</slot>
    </button-component-basic>
  </div>
</template>

<script>
import ButtonComponentBasic from "@/components/componentsSimple/ButtonComponentBasic";
import InputComponentBasic from "@/components/componentsSimple/InputComponentBasic";
import ModalComponentBasic from "@/components/componentsSimple/ModalComponentBasic";
export default {
  name: "InputWithModalGroup",
  data(){
    return {
      opened: true,
      someData: ''
    }
  },
  props:{
    btnName:String,
    listName: Array
  },
  components: {
    ModalComponentBasic, InputComponentBasic,ButtonComponentBasic
  },
  methods: {
    clickEvent(){
      this.opened = !this.opened;
    },
    sendList(){
      this.someData = this.listName
    }
  }
}
</script>

<style scoped>
  .wrap{
    display: flex;
  }
</style>