<script setup>
import { ref } from 'vue'

const isLogin = ref(false)
const type = ref('D')
const status = ref('offline')
const handleStatus = () => {
  if (status.value === 'online') {
    status.value = 'offline'
  } else if (status.value === 'offline') {
    status.value = 'Không xác định'
  } else {
    status.value = 'online'
  }
}


const isActive= ref(false)
</script>

<template>
  <div>
    <div>
      <h1 v-show="isActive"> Window is active</h1>

    </div>






    <h1 v-if="isLogin">Chào mừng bạn đã đăng nhập</h1>
    <h1 v-else>Chào mừng bạn đã đăng xuất</h1>

    <div>
      <p v-if="status === 'online'">Bạn đang online</p>
      <p v-else-if="status === 'offline'">Bạn đã offline</p>
      <p v-else>Không xác định</p>
      <button @click="handleStatus">Change Status</button>
    </div>

    <div>
      <div v-if="type === 'A'">A</div>
      <div v-else-if="type === 'B'">B</div>
      <div v-else-if="type === 'C'">C</div>
      <div v-else>Not A/B/C</div>
    </div>




  </div>
</template>

<style lang="scss">
</style>
