<template>
  <div class="home">
    <img alt="Vue logo" src="../../public/images/layout/logo.png">
    <HelloWorld />
  </div>
</template>

<script>
  // @ is an alias to /src
  import HelloWorld from '@/components/HelloWorld.vue'

  export default {
    name: 'home',
    components: {
      HelloWorld
    }
  }
</script>
