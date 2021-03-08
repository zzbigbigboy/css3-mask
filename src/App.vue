<template>
  <div class="app_body">
    <A />
    <B />
    <C />
    <DD />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import A from './components/A.vue';
import B from './components/B.vue';
import C from './components/C.vue';
import DD from './components/DD.vue';

export default {
  name: 'App',
  components: {
    A,
    B,
    C,
    DD,
  }
}
</script>

<style>
html body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
.app_body {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}
</style>
