<script setup>
import { reactive, ref } from 'vue'
// Binding Class
// 2 cách : Object and Array
// với cách truyền đối tượng, với dữ liệu là Truethy thì nó sẽ add key của nó vào

const isBox = ref(false)
const classObject = reactive({
  button: true,
  active: true,
  'has-error': true
})

const color = ref('red')
const fontSize = ref(30)
</script>

<template>
  <div>
    <div :class="{ box: isBox }">Box</div>
    <button :class="classObject">Active</button>

    <div :style="{ color, fontSize: fontSize + 'px' }">Style binding</div>
  </div>
</template>

<style lang="scss">
.box {
  width: 300px;
  height: 300px;
  background-color: blue;
}

.button {
  color: white;
  background-color: #3247c9;
  border: none;
  padding: 10px 14px;
  border-radius: 6px;
  &:hover {
    background-color: #6070d1;
  }
}
.active {
  color: #c860d1;
  background-color: #e6b2eb;
  &:hover {
    background-color: #ae96b0;
  }
}
.has-error {
  border: 1px solid #bd2e24;
  color: white;
  background: #bd2e24;
}
</style>
