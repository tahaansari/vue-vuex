<template>
  <div>
      <h3>TODOS</h3>
      <div class="todos">
          <div  class="todos__todo" v-for="todo in getTodos" :key="todo.id" v-bind:class="{'todos__completed': todo.completed }" @click="toggleCompleted">
              {{ todo.title }}
              <i @click="deleteTodo(todo.id)" class="todos__del fa fa-trash"></i>
          </div>
      </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'
export default {
    methods:{
        ...mapActions(['fetchTodos','deleteTodo']),
        toggleCompleted(event){
            event.target.classList.toggle('todos__completed')
        }
    },
    computed: {
        ...mapGetters(['getTodos'])
    },
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
        color: #ffffff;
        padding: 20px;
        border: 1px solid #ffffff;
        cursor: pointer;
    }
    &__del{
        cursor: pointer;
        float: right;
    }
    &__completed{
        background: black;
        text-decoration: line-through;
    }
}
</style>