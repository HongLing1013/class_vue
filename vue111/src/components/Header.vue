<script setup>
// 解構函式
import { ref } from 'vue';

const props=defineProps({
  headerStr:String,
})

const name=ref('hollie')

const header=ref(props.headerStr)
const sayHi=()=>{
  header.value=prompt("請輸入你要更改的標題")
}

</script>
<template>

<h1>{{ header }}</h1>
<button @click="sayHi">SayHi</button>
<br />
<!-- input輸入後在p內顯示文字內容 -->
<p>{{ name }}</p>
<input type="text" v-model="name">

</template>
<style scoped>

  /* scoped會使下面的css只對此檔案的vue內容生效 */
h1{
  color:red;
}
button{
  background-color: aqua;
  color: blue;
  box-shadow: 0.25rem 0.25rem 10px blue;
}
p{
    font-size: 2.5rem;
    color:blue;
    text-shadow: 2px 2px 10px skyblue;
  }
</style>