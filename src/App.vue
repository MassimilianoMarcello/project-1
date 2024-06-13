<template>
  <div id="app">
    <div class="square" :style="{ left: left + 'px' }">
      <h1>I am a square</h1>
    </div>
    <button @click="moveSquare">Move Square</button>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'App',
  setup() {
    const left = ref(0);

    const moveSquare = () => {
      left.value += 10;
    };

    return {
      left,
      moveSquare
    };
  }
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
.square {
  height: 10rem;
  width: 10rem;
  background-color: green;
  position: relative;
}
.square h1 {
  color: red;
}
button {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 16px;
}
</style>
