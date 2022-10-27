<script setup lang="ts">
const bgColor = ref('#a221a1')
const textA = ref('W')
const textB = ref('M')
function goPath() {
  window.open('https://www.remove.bg/zh/upload')
}
</script>

<template>
  <div flex justify-center>
    <div
      class="card" :style="{
        'background': bgColor, 'box-shadow': `inset -20px -20px 60px ${bgColor},
    inset 20px 20px 60px #ccc`,
      }"
    >
      <span> {{ textA }} </span>
      <span class="right"> {{ textB }} </span>
    </div>
    <div class="tools">
      <!-- <div class="tools-item">
        字母A: <input v-model="textA" type="text">
      </div>
      <div class="tools-item">
        字母B: <input v-model="textB" type="text">
      </div> -->
      <div class="tools-item">
        卡片颜色: <input v-model="bgColor" type="color">
      </div>
      <div class="tools-item">
        <button btn @click="goPath">
          处理logo
        </button>
      </div>
    </div>
  </div>
</template>

<style>
.card span {
  text-align: left;
  display: inline-block;
  line-height: 100px;
  vertical-align: text-top;
  margin-left: 13px;
}

.card .right {
  position: absolute;
  bottom: 40px;
  left: 60px;
}

.card {
  border-radius: 50px;
  font-family: auto;
  text-align: left;
  position: relative;
  font-weight: bold;
  width: 180px;
  height: 100px;
  color: #fff;
  font-size: 100px;
  padding: 50px 0px;
  padding-left: 20px;
  box-sizing: content-box;

}

.tools {
  margin-left: 20px;
}

.tools-item {
  text-align: left;
  /* justify-content: center; */
  margin: 10px 0;
}

input {
  border: 1px solid rgba(1, 1, 1, 0.2);
  padding-left: 10px;
}
</style>

<route lang="yaml">
meta:
  layout: home
</route>
