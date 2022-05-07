<script>
export default {
  data () {
    return{
      todo: '',
      savedTodo: [],
    }
  },
  methods: {
    saveTodo(){
      this.savedTodo.push(this.todo),
      this.todo = ''
    },
    deleteTodo(index){
      this.savedTodo.splice(index, 1)
    }
  }
}
</script>

<template>
  <section class="todo">
      <h1 class="todo_title">Todo List App</h1>
      <p>Create your tasks here</p>
      <div class="todo_action">
        <input class="todo_input" v-model="todo" type="text">
        <button class="todo_save" @click="saveTodo">Save</button>
      </div>
  </section>
  <section class="list">
    <div class="list_task" v-for="(todo, index) in savedTodo" :key="index">
      <div class="list_content">{{ todo }}</div>
      <button class="list_delete" @click="deleteTodo(index)">Delete</button>
    </div>
  </section>
</template>

<style scoped>
.todo_title {
  font-size: 50px;
  margin-bottom: 10px;
}

.todo_action {
  display: flex;
  justify-content: center;
  align-items: center;
}

.todo_input{
  border:none;
  outline: none;
  border-bottom: 1px solid #fff;
  background-color: transparent;
  color: #fff;
  font-size: 25px;
  padding: 10px 0;

}
</style>
