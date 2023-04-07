<template>
  <Management />
</template>

<script>
import Login from "@/pages/Login.vue"
import Management from "@/pages/Management.vue";

export default {
  name: 'App',
  components: {
    Login,
    Management
  }
}
</script>

<style>
html, body, #app {
  height: 100%;
  user-select: none;
}

body {
  margin: 0;
  font-size: 12px;
  line-height: 20px;
  font-family: Microsoft Yahei;
  overflow: scroll;
}
</style>
