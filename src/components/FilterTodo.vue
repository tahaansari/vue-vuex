<template>
  <div>
      Filter
      <select @change="changeFilter" name="" id="">
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
        ...mapActions(['changeFilter']),
        changeFilter(event){
            console.log(event)
            console.log(event.target)
            // console.log('filter change called ',event.options[event.selectedIndex].value)
            // this.changeFilter(event.)
        }
    }
}
</script>

<style>

</style>