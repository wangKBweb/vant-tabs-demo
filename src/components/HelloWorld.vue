<script setup lang="ts">
import { ref } from 'vue'
import { Tab, Tabs } from 'vant'
import 'vant/lib/index.css'


const tabs = ref(Array(3).fill(''))

const active = ref(0)

</script>

<template>
  <div class="HelloWorld">
    <Tabs v-model:active="active" animated sticky swipeable>
      <Tab v-for="index in tabs" :title="'选项 ' + index">
        <div class="items">
          <div class="item" v-for="index in 30">
            {{ index }}
          </div>
        </div>
      </Tab>
    </Tabs>
  </div>
</template>

<style scoped>
/* 复现只需要解开下面HellowWorld的注释 */
/* .HelloWorld {
  height: 1000px;
  overflow-y: auto;
} */
.items {
  padding: 10px;
}
.item {
  width: 100%;
  height: 80px;
  border: 1px solid gray;
  margin-bottom: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 20px;
}
</style>
