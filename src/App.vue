<template>
  <div>
    <h1>TODO APP</h1>
    <PostTodo @onClick="postTodo" />
    <div>TODO一覧</div>
    <ul v-for="(todo, i) in todos" :key="i">
      <ListTodo :todo="todo" />
    </ul>
  </div>
</template>

<script>
import PostTodo from "./components/PostTodo.vue";
import ListTodo from "./components/ListTodo.vue";

export default {
  components: {
    PostTodo,
    ListTodo,
  },
  data() {
    return {
      todos: [],
    };
  },
  methods: {
    postTodo(value) {
      this.todos.push({
        todo: value,
        isCheck: false,
      });
    },
  },
};
</script>
