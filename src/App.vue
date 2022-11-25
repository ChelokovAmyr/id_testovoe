<template>
  <div class="component-wrap">
  <InputSimpleGroup
    id="username"
    name="username"
    v-model="inputSimple"
    label="Лейбл"
    required
  />
  </div>
  <div class="component-wrap">
  <InputWithBtnGroup
    v-model="inputWithBtn"
    btnName="Клик по кнопке"
  />
  </div>
  <div class="component-wrap">
  <InputWithModalGroup
    v-model="inputWithModal"
    btnName="Вызов модалки"
    :listName="listName"
  />
  </div>
</template>

<script>
import InputSimpleGroup from './components/componentGroup/InputSimpleGroup.vue'
import InputWithBtnGroup from './components/componentGroup/InputWithBtnGroup.vue'
import InputWithModalGroup from './components/componentGroup/InputWithModalGroup.vue'

export default {
  name: 'App',
  data(){
    return {
      inputOne:'',
      inputTwo:'',
      inputThree: '',
      listName: [
          'Я',
          'Хочу',
          'Новую',
          'Работу'
      ]
    }
  },
  components: {
    InputSimpleGroup,
    InputWithBtnGroup,
    InputWithModalGroup
  },
  computed: {
    inputSimple:{
      get(){
        return this.inputOne
      },
      set(value){
        this.inputOne = value
      }
    },
    inputWithBtn:{
      get(){
        return this.inputTwo
      },
      set(value){
        this.inputTwo = value
      }
    },
    inputWithModal:{
      get(){
        return this.inputThree
      },
      set(value){
        this.inputThree = value
      }
    },
  }
}
</script>

<style>
</style>
