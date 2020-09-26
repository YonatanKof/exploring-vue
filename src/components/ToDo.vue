<template>
  <div id="todo-list">
    <form v-on:submit.prevent="addNewTodo">
      <label class="title" is="h2" for="new-todo">Add a todo</label>
      <span class="set-todo">
        <input
          v-model="newTodoText"
          id="new-todo"
          placeholder="E.g. Feed the cat"
        />
        <button>Add</button>
      </span>
    </form>
    <ul>
      <li
        is="todo-item"
        v-for="todo in todos"
        :key="todo.id"
        :title="todo.title"
      >
        {{ todo.title }}
        <button @click="removeTodo(todo.id)">Remove</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ToDoList",

  data() {
    return {
      newTodoText: "",
      props: ["title"],
      todos: [
        {
          id: 1,
          title: "Do the dishes",
        },
        {
          id: 2,
          title: "Take out the trash",
        },
        {
          id: 3,
          title: "Mow the lawn",
        },
      ],
      nextTodoId: 4,
    };
  },
  methods: {
    addNewTodo() {
      this.todos.push({
        id: this.nextTodoId++,
        title: this.newTodoText,
      });
      this.newTodoText = "";
    },
    removeTodo(id) {
      const index = this.todos.findIndex((item) => item.id == id);
      this.todos.splice(index, 1);
    },
    // removeToDo() {
    //   this.todos.splice(index, 1);
    // },
  },
};
</script>

<style lang="scss" scoped>
#todo-list {
  text-align: left;
}
.title{
  margin: 0.25em 0;
}
form {
  display: flex;
  flex-direction: column;
  margin-bottom: 1em;
}
ul {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
}
todo-item {
  margin: 0.25em 1em 0.25em 0;
  font-size: 1.1em;
  button {
    margin-left: 1em;
    background-color: lightpink;
  }
}
</style>