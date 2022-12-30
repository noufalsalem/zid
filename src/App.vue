<script lang="ts">
  import { defineComponent } from 'vue';
  import Sidebar from './components/Sidebar.vue'

  export default defineComponent({
    name: 'App',
    components: { Sidebar }
  })
</script>
<template>
  <Sidebar />
  <router-view/>
</template>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #84589D;
}

</style>
