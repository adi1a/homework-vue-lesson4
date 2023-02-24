<template>
  <div id="app">
    <TopbarComponent />
    <router-view />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import TopbarComponent from './components/Topbar.vue';
import ContainerComponent from './components/Container.vue';

export default Vue.extend({
  name: 'App',
  components: {
    TopbarComponent,
    ContainerComponent,
  },
});
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body{
  font-family: sans-serif;
}

ul{
  list-style: none;
}
</style>
