<template>
<div>
    <div class="square" :style="{ left: left + 'px' }">
      <h1>I am a square</h1>
    </div>
    <button @click="moveSquareToRight">Move Right +100</button>
    <button @click="reset" >Reset</button>
    <button @click="moveSquareToLeft" >Left -10</button>
  
</div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'MovetheBox',
  setup() {
    const left = ref(0);

    const moveSquareToRight = () => {
      if (left.value < 1000) {
        left.value += 100;
      }
    };
    const moveSquareToLeft = () => {
      if (left.value > 10) {
        left.value -= 10;
      }
    };
    const reset = () => {
   left.value=0;
    };

    return {
      left,
      moveSquareToRight,
      moveSquareToLeft,
      reset,
    };
  }
};
</script>

<style>

.square {
  height: 100px;
  width: 100px;
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
