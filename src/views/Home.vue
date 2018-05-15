<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/Landing.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  }
}
</script>
<style>
.home {
  min-height: 100%;
  min-width: 100%;
}
</style>
