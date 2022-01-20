<template>
  <div id="app">
    <h1>TO DO:</h1>
    <ToDo textContent="" :done="false" />
    <ToDoList :dataList="dataList" />
  </div>
</template>

<script>
import ToDo from "./components/ToDo";
import ToDoList from "./components/ToDoList.vue";

export default {
  name: "App",
  components: {
    ToDo, ToDoList
  },
  data() {
    return {
      dataList: [
        {
          text: 'get up at 10 am',
          done: false,
        },
        {
          text: 'visit God in prayer',
          done: true,
        },
        {
          text: 'code a few lines',
          done: true,
        },
        {
          text: 'end the day',
          done: false,
        },
        {
          text: 'repeat the same',
          done: true,
        }
      ]
    }
  }
};
</script>

<style>
#app {
  font-family: "Roboto", helvetica, arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  padding: 60px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;

  background: linear-gradient(
    135deg,
    rgba(65, 184, 131, 0.9),
    rgba(52, 73, 94, 0.9)
  );

  font-size: 1.5em;
}
</style>
