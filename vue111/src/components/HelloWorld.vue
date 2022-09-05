<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
  user: String
})

const count = ref(0)
const count1 = ref(1)
// 資料歸資料 資料不影響畫面呈現 兩者是分開的
</script>

<template>
  <h1>{{ msg }}</h1>
  <h1>{{ user }}</h1>

  <div class="card">
    <!-- 第一個button按一下數字+1 第二個button按下去資料是雙倍的+上去 -->
    <button type="button" @click="count++">count is {{ count }}</button> 
    <button type="button" @click="count1=count1*2">count is {{ count1 }}</button>
    <!-- 畫面歸畫面 畫面不影響資料內容 兩者是分開的 -->
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
