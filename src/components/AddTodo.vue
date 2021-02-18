<template>
  <div>
      <h3>Add Todo</h3>
      <div class="add-todo">
          <form @submit.prevent="submitTodo" class="add-todo__form">
            <input class="add-todo__input" v-model="todoTitle" type="text" placeholder="Add todo..">
            <input class="add-todo__submit" type="submit" value="Add">
          </form>
      </div>
  </div>
</template>

<script>
import {mapActions} from 'vuex'
export default {
    data(){
        return{
            todoTitle:""
        }
    },
    methods:{
        ...mapActions(['addTodo']),
        submitTodo(){
            if(this.todoTitle!=""){
                this.addTodo(this.todoTitle);
            }
        }
    }
}
</script>

<style lang="scss" scoped>
.add-todo{
    &__form{
        display: flex;
    }
    &__input{
        width: 100%;
        padding: 10px;
        border: 1px solid black;
        border-right: 0;
    }
    &__submit{
        background-color: green;
        border: 1px solid green;
        color: #ffffff;
        padding: 10px 30px;
        border: none;
    }
}
</style>