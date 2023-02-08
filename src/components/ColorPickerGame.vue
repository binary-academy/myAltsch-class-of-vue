<template>
  <div class="container">
    <h1>Color Picker Game</h1>

    <div>{{ message }}</div>

    <button v-for="color in colors" :key="color" @click="matchColor(color)">
      {{ color }}
    </button>
  </div>
</template>

<script>
import ColorPicker from "../composables/ColorPicker";
export default {
  name: "ColorPickerGame",
  data() {
    return {
      colors: [],
      message: "",
    };
  },
  methods: {
    matchColor() {},
  },
  setup() {
    const { colors, message, matchColor } = ColorPicker();
    return { colors, message, matchColor };
  },
};
</script>

<style>
.container {
  text-align: center;
  padding: 1rem;
  border: 1px dashed grey;
}

button {
  padding: 10px 20px;
  margin: 10px 5px;
  border: 1px solid grey;
  border-radius: 5px;
}
</style>
