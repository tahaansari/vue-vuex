<template>
  <div id="app">
    <div class="container">
      <AddTodo/>
      <br>
      <FilterTodo/>
      <Todos/>
    </div>
  </div>
</template>

<script>
import AddTodo from './components/AddTodo'
import FilterTodo from './components/FilterTodo'
import Todos from './components/Todos'

export default {
  name: 'App',
  components: {
    AddTodo,
    FilterTodo,
    Todos,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
*{
  box-sizing: border-box;
}
body{
  font-family: 'Roboto', sans-serif;
}
</style>