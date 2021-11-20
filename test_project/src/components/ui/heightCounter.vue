<template>
  <div class="counter">
    <div
      class="value-button"
      id="decrease"
      @click="increaseValue"
      value="Decrease Value"
    >
      <font-awesome-icon class="arrow-icon" icon="caret-up" />
    </div>
    <input type="number" id="number" value="0" />
    <div
      class="value-button"
      id="increase"
      @click="decreaseValue"
      value="Increase Value"
    >
      <font-awesome-icon class="arrow-icon" icon="caret-down" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    msg: String,
  },

  methods: {
    increaseValue() {
      console.log("sdffs");
      var value = parseInt(document.getElementById("number").value, 10);
      value = isNaN(value) ? 0 : value;
      value++;
      document.getElementById("number").value = value;
    },

    decreaseValue() {
      var value = parseInt(document.getElementById("number").value, 10);
      value = isNaN(value) ? 0 : value;
      value < 1 ? (value = 1) : "";
      value--;
      document.getElementById("number").value = value;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.counter {
  display: inline-block;
}
.arrow-icon {
  color: rgb(1, 3, 119);
  font-size: 30px;
}
.value-button {
  margin: 0px;
  width: 39px;
  text-align: center;
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.value-button:hover {
  cursor: pointer;
}

input#number {
  text-align: center;
  border: none;
  font-size: 15px;
  font-weight: bold;

  margin: 0px;
  width: 40px;
}

input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;
}
</style>
