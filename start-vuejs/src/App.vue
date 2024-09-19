<script setup>
import { ref, reactive } from 'vue'
// 2 cách binding style : qua đối tượng và qua mảng

const isActive= ref(false)
const hasError = ref(true)

const classObject = reactive({
  active: true,
  'has-error': false

})

const color = ref('blue')
</script>

<template>
  <div>
    <button class="button" :class="classObject">Button</button>

    <p :style="{ color }">Demo style</p>
  </div>
</template>

<style lang="scss" scoped>
.button {
  border: none;
  background: #ede9fe;
  color: #8b5cf6;
  padding: 10px 14px;
  border-radius: 6px;
  cursor: pointer;
  &:hover {
    background: #c7d2fe;
  }
}
.active {
  background: #8b5cf6;
  color: #ede9fe;
  &:hover {
    background: #818cf8;
  }
}
.has-error {
  color: #d63024;
  border: 1px solid red;
  background: #fee2e2;
  &:hover {
    background: #fee2e2;
  }
}
</style>
