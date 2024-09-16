<script setup>
// 1.Text Interpolation
const title = 'Template Syntax'
// cú pháp khai báo + tên biến = giá trị của biến

// 2.Raw HTML
const content = '<span>Raw HTML</span>'

// 3.Attribute Bindings and Shorthand
const dynamicId = 'dynamic-id-1'


// 4.Boolean Attributes

const isClick = true
// v-bind:disabled="isClick"

// v-bind cú pháp  cua vue : thuộc tính của thẻ html = biến ở trong phần script
// : thuộc tính của thẻ html = biến ở trong phần script

// Bài tập, tạo ra 2 thẻ div bao gồm: tên, tuổi và 1 nút button submit
// thêm id name vào trong thẻ div chứ tên
// thêm id age vào trong thẻ div chứ tuổi và đổi màu thành màu đỏ
// thêm id btn vào trong thẻ button
// và thêm 1 thuộc tính disable  có giá trị là biến btn-disable = true trong script



// 5.Dynamically Binding Multiple Attributes
// Truyền động nhiều thuộc tính dữ liệu
const box = {
  id:'content1',
  class: 'content',
  style: 'padding:10px'
}

</script>

<template>
  <div>
    <div>{{ title }}</div>
    <span id="content" v-html="content"></span>
    <p v-bind:id="dynamicId">Lê văn Hiển</p>
    <button :disabled="isClick"  >click</button>
    <p v-bind="box">box</p>
    <!-- Demo bootstrap -->
     <p class="text-primary">text-primary</p>

  </div>
</template>

<style>
#dynamic-id-1{
  color: yellow
}
</style>
