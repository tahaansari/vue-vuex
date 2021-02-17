<template>
  <div>
      <div class="todos">
          <div class="todos__todo" v-for="todo in allTodos" :key="todo.id">
              {{ todo.title }}
          </div>
      </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex'
export default {
    methods:{
        ...mapActions(['fetchTodos'])
    },
    computed:mapGetters(['allTodos']),
    created(){
        this.fetchTodos()
    }
}
</script>

<style lang="scss">
.todos{
    display: flex;
    flex-wrap: wrap; 
    &__todo{
        width: 50%;
        background: green;
        padding: 20px;
        border: 1px solid #ffffff;
    }
}
</style>