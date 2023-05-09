<template>
  <li>
    <input type="checkbox" />
    todoの内容は <b>{{ todo }}</b>
  </li>
</template>

<script>
export default {
  props: ["todo"],
};
</script>
