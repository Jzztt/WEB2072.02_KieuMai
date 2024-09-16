<script setup>
import { nextTick , ref } from 'vue'
// bước 1: theo dõi
// nước 2: cập nhật

const count = ref(1)

const handleCount = async () => {
  count.value++
  console.log([document.getElementById('count')]);
  console.log('step1', document.getElementById('count').innerText);
  await nextTick()
  console.log('step2', document.getElementById('count').innerText);

}
// Bài tập 1, Tao 1 ref lưu trữ giá ban đầu là 100, và sau do tạo 1 nut button click, mỗi lần click tăng thêm 1 đơn vị
// Bài tập 2, hãy lưu dữ liệu cá nhân( tên, tuổi, mssv, sđt, email) và reactivity sau đó hiển thị ra ngoài giao diện

</script>

<template>
  <div>
    <div id="count">{{ count }}</div>
    <button @click="handleCount">Count</button>
  </div>

</template>

<style>

</style>
