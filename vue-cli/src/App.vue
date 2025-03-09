<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1 class="test">Test</h1>
<Class />
</template>

<script>
import Class from './components/MyClass.vue';

export default {
  name: 'App',
  components: {
    Class,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.test{
  background-color: red;
}
</style>
