<template>
  <div>
    <header>
      <h1>To Do List</h1>
    </header>

    <div>
      <ul>
        <li v-for="task in tasks" v-bind:key="task.id">{{task}}</li>
      </ul>
    </div>
  </div>
</template>

// script is for static data like state or javascript
<script>
export default {
  data() {
    return {
      tasks: [
        {
          text: "Learn Vue",
          done: false
        },
        {
          text: "Become software engineer",
          done: false
        }
      ]
    };
  }
};
</script>

<style scoped>
</style>
