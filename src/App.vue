<template>
  <div id="app">
    <div class="container">
      <todos/>
    </div>
  </div>
</template>

<script>
import todos from './components/Todos'

export default {
  name: 'App',
  components: {
    todos,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
*{
  margin: 0;
  padding: 0;
  font-weight: normal; 
  line-height: 1;
  box-sizing: border-box;
}
body{
  font-family: 'Roboto', sans-serif;
  background: #333333;
  color: #ffffff;
}
</style>