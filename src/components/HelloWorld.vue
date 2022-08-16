<template>
  <div class="hello">
    <div class="msg">{{state.msg}}</div>
    <button @click="add">{{state.count}} </button>
  </div>
</template>

<script>

import { reactive } from 'vue'

export default {
   setup (){
     const state = reactive({count:0, msg:'哈哈哈'})
     const add = ()=>{
       state.count++
       if (state.count == 10) {
           state.msg = '9999'
       }
     }

     return {state,add}
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
   padding-left: 20px;
   padding-right: 20px;
  height: 100px;
  background-color: bisque;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.hello .msg {
  font-size: 16;
  color: #333333;
  padding-bottom: 10px;
}

button{
  color: white;
  font-size: 18px;
  border: 0ch;
  background-color: aqua;
}
</style>
