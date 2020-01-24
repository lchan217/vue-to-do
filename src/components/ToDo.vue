<template>
  <div>
    <header>
      <h1>To Do List</h1>
      <input placeholder="what needs to be done?" v-model='newTask' @keyup.enter="addTask($event)"></input>
    </header>

    <div>
      <ul>
        <li v-for="task in tasks" v-bind:key="task.id">{{task.text}}</li>
      </ul>
    </div>
  </div>
</template>

// script is for static data like state or javascript
<script>
export default {
  data() {
    return {
      newTask: "",
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
  }, 

  methods: {
      addTask(event){
          this.tasks.push({text: this.newTask, done: false})
          this.newTask=''
      }
  }
};
</script>

<style scoped>
</style>
