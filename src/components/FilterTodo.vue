<template>
  <div>
      Filter
      <select @change="changeFilter" name="" id="filter_todo">
          <option value="200">200</option>
          <option value="150">150</option>
          <option value="100">100</option>
          <option value="50">50</option>
          <option value="20">20</option>
          <option value="10">10</option>
          <option value="5">5</option>
      </select>
  </div>
</template>

<script>
import {mapActions} from 'vuex'
export default {
    name:"FilterTodo",
    methods:{
        ...mapActions(['filterTodo']),
        changeFilter(){
            let filterValue = document.querySelector('#filter_todo').value;
            this.filterTodo(filterValue)
        }
    }
}
</script>

<style>

</style>