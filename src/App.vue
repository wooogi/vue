<template>
  <div id="app">
    <div id="wapper">
      <heade />
      <router-view/>
      <foot />
    </div>
  </div>
</template>
<script>
  import footer from '@/components/Footer.vue'
  import header from '@/components/Header.vue'
  import '@/assets/css/common.css';
  import $ from 'jquery';

  export default {
    components: {
      'foot' : footer,
      'heade' : header
    }
  }
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>