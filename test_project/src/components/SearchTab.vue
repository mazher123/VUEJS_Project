<template>
  <div class="col-4 searchtab">
    <div class="row search-header">
      <div class="col-2">
        <custom-button
          width="100px"
          height="30px"
          icon="caret-left"
          labelcolor="rgb(1, 3, 119)"
          color="#fff"
          radius="20px"
        >
          Back
        </custom-button>
      </div>
      <div class="col-10">
        <h3>Search Manager</h3>
      </div>
    </div>

    <div class="row justify-content-md-center load-section">
      <div class="left">
        <span>
          <font-awesome-icon class="arrow-icon2" icon="caret-left"
        /></span>
      </div>
      <div class="col-10 text-center load-buttons">
        <custom-button
          width="120px"
          height="30px"
          icon="spinner"
          labelcolor="#fff"
          color=" rgb(1, 3, 119)"
          radius="20px"
        >
          Save Search
        </custom-button>

        <custom-button
          width="160px"
          height="30px"
          icon="redo-alt"
          labelcolor="#fff"
          color=" rgb(1, 3, 119)"
          radius="20px"
        >
          Load Save Search
        </custom-button>
        <!-- 
        <button>Save Search</button> <button>Load Saved Search</button> -->
      </div>
    </div>
    <hr />
    <div class="row">
      <div class="col-2 label">Age :</div>
      <div class="col-10 age"><AgeRange :trackHeight="0.5" /></div>
    </div>
    <hr />

    <div class="row">
      <div class="col-2 label">Height :</div>

      <div class="col">
        <heightCounter :key="1"></heightCounter>
        <span class="counter-dot"> .</span>
        <heightCounter :key="2"></heightCounter>
      </div>

      <div class="col">
        <div class="metric">
          <div class="custom-radios">
            <div>
              <input
                type="radio"
                id="color-1"
                name="color"
                value="color-1"
                checked
              />
              <label for="color-1">
                <span> CM </span>
              </label>
            </div>

            <div>
              <input type="radio" id="color-2" name="color" value="color-2" />
              <label for="color-2">
                <span> M </span>
              </label>
            </div>
          </div>
        </div>
        <div class="separator">
          <!-- <span class="separator-left">-</span> -->
          <h3 class="separator-label">To</h3>
          <!-- <span class="separator-right">-</span> -->
        </div>
      </div>
      <div class="col">
        <heightCounter :key="1"></heightCounter>
        <span class="counter-dot"> .</span>
        <heightCounter :key="2"></heightCounter>
      </div>
    </div>

    <hr />
    <div class="row select-option">
      <div class="col">
        <CustomSelect
          :options="['Islam', 'buddha', 'Christan', 'hindu']"
          :default="'Religion'"
          class="select"
          @input="alert(displayToKey($event))"
        />
        <CustomSelect
          :options="['Bangladesh', 'India', 'UK', 'USA']"
          :default="'Country'"
          class="select"
          @input="alert(displayToKey($event))"
        />
        <CustomSelect
          :options="['national', 'tribal', 'lingustic', 'religious']"
          :default="'Ethnicity'"
          class="select"
          @input="alert(displayToKey($event))"
        />
        <CustomSelect
          :options="['single', 'married', 'divorced', 'complicated']"
          :default="'Marital Status'"
          class="select"
          @input="alert(displayToKey($event))"
        />
      </div>
    </div>
    <div class="row select-option">
      <div class="col-12"><h3 class="label text-center">Tags</h3></div>
      <div class="col-12">
        <input-tag v-model="tags"></input-tag>
      </div>
    </div>
    <div class="row select-option text-center">
      <custom-button
        width="200px"
        height="40px"
        icon="search-location"
        labelcolor="#ffff"
        color="rgb(1, 3, 119)"
      >
        Search
      </custom-button>
    </div>
    <div class="row">
      <div class="col-12">
        <p class="text-center"><a href="#"> Advance Search</a></p>
      </div>
    </div>
  </div>
</template>

<script>
import AgeRange from "./ui/Range.vue";
import heightCounter from "./ui/heightCounter.vue";
import CustomSelect from "./ui/CustomSelect.vue";
import CustomButton from "./ui/CustomButton.vue";
import InputTag from "vue-input-tag";

export default {
  components: { AgeRange, heightCounter, CustomSelect, InputTag, CustomButton },
  name: "searchTab",
  data() {
    return {
      tags: "",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.arrow-icon2 {
  color: rgb(235, 235, 240);
  font-size: 30px;
  position: relative;
  top: 22px;
}
.left {
  width: 47px;
  height: 79px;
  border-bottom-left-radius: 90px;
  border-top-left-radius: 90px;
  background: rgb(1, 3, 119);
  position: relative;

  left: 563px;
  z-index: 9999;
  bottom: 56px;
  border: 2px solid #fff;
}
.select-option {
  margin-bottom: 10px;
}
.separator-left {
  content: "-";
  position: relative;
  left: -1rem;
  font-weight: bold;
  color: black;
}
.separator-right {
  content: "-";
  position: relative;
  left: -1rem;
  font-weight: bold;
  color: black;
}
.separator-label {
  font-size: 20px;
  font-weight: bold;
  font-family: "oswald";
  color: rgb(1, 3, 119);
  padding-top: 10px;
  margin-left: 5px;
}
.counter-dot {
  position: relative;
  font-size: 35px;
  font-weight: bold;
  bottom: 33px;
  right: 5px;
}
.label {
  font-size: 20px;
  font-weight: 600;
  font-family: "oswald";
}
.searchtab {
  border-radius: 18px;
  border: 2px solid rgb(150, 150, 150);
  box-shadow: 3px #333;
  padding: 10px;
}
.search-header {
  background: rgb(1, 3, 119);
  padding: 10px;
}
.search-header h3 {
  color: #fff;
  margin-left: 97px;
}
.load-section {
  margin-top: 10px;
}
.load-buttons {
  padding-bottom: 20px;
}

.custom-radios div {
  display: inline-block;
}
.custom-radios input[type="radio"] {
  display: none;
}
.custom-radios input[type="radio"] + label {
  color: #333;
  font-family: Arial, sans-serif;
  font-size: 14px;
}
.custom-radios input[type="radio"] + label span {
  display: inline-block;
  width: 30px;
  height: 18px;
  margin: -1px 4px 0 0;
  cursor: pointer;
  box-shadow: 0 1px 3px 0 rgb(0 0 0 / 33%);
  background-repeat: no-repeat;
  background-position: center;
  text-align: center;
  color: #ffff;
}
.custom-radios input[type="radio"] + label span img {
  opacity: 0;
  transition: all 0.3s ease;
}
.custom-radios input[type="radio"]#color-1 + label span {
  background-color: rgb(1, 3, 119);
}
.custom-radios input[type="radio"]#color-2 + label span {
  background-color: #ffff;
  color: #333 !important;
}
</style>
