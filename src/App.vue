<template>
  <div id="app">
    <MovetheBox />
  </div>
</template>

<script>
import MovetheBox from './components/MoveTheBox'; // Adjust path as necessary

export default {
  components: {
    MovetheBox,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #632159;
  margin-top: 60px;
  position: relative;
}
</style>
