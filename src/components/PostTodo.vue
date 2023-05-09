<template>
  <div>
    <input type="text" v-model="inputTodo" />
    <button @click="postTodo">送信</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputTodo: "",
    };
  },
  methods: {
    postTodo() {
      this.$emit("onClick", this.inputTodo);
      this.inputTodo = "";
    },
  },
};
</script>
