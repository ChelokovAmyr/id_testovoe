<template>
  <div class="modal-window" v-if="opened">
    <slot v-if="listName">
        <p v-for="item in listName" :key="item" @click="sendList" class="list-item">
          {{item}}
        </p>
    </slot>
  </div>
</template>

<script>
export default {
  name: "ModalComponentBasic",
  props:{
    listName:Array,
    opened: Boolean
  },
  data(){
    return{

    }
  },
  methods: {
    sendList(){
      this.$emit('sendList')
    }
  }
}
</script>

<style scoped>
.list-item{
  display: inline-block;
  margin-right: 10px;
}
</style>