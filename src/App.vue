<template>
  <div id="app">
    <keep-alive>
      <!-- 路由过一次后，存入内存中，下次在访问，从内存中获取 -->
      <router-view />
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style></style>
