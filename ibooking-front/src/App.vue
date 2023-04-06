<template>
  <Login />
</template>

<script>
import Login from "@/pages/Login.vue"

export default {
  name: 'App',
  components: {
    Login
  }
}
</script>

<style>
body {
  margin: 0;
  font-size: 12px;
  line-height: 20px;
  background-color: #F7F8FC;
  font-family: Microsoft Yahei;
  background-image: url("~@/assets/cas_bg.png");
  overflow: hidden;
}
</style>
