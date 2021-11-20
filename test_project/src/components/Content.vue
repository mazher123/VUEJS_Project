<template>
  <div class="col-8 content">
    <div class="row">
      <div class="col-12">
        <h1>Search Results</h1>
      </div>
    </div>

    <div class="row">
      <div class="col-6">
        <p>Matches for your requirements : 25 results</p>
      </div>
      <div class="col-3">
        <custom-button
          width="200px"
          height="30px"
          icon="redo-alt"
          labelcolor="#fff"
          color=" rgb(1, 3, 119)"
          radius="20px"
        >
          Manage Filter
        </custom-button>
      </div>
      <div class="col-3">
        <custom-button
          width="200px"
          height="30px"
          icon="redo-alt"
          labelcolor="#fff"
          color=" rgb(1, 3, 119)"
          radius="20px"
        >
          Advance Search
        </custom-button>
      </div>
    </div>
    <div class="row filters">
      <div class="col-4">
        <custom-button
          width="50px"
          height="30px"
          icon="bars"
          labelcolor="#fff"
          color=" rgb(1, 3, 119)"
          radius="5px"
        >
        </custom-button>
        &nbsp;
        <custom-button
          width="50px"
          height="30px"
          icon="caret-square-down"
          labelcolor="#fff"
          color=" rgb(1, 3, 119)"
          radius="5px"
        >
        </custom-button>
      </div>
      <div class="col-8">
        <ul class="nav justify-content-end">
          <li class="nav-item">
            <div class="chip">
              John Doe
              <span>x</span>
            </div>
          </li>
          <li class="nav-item">
            <div class="chip">
              John Doe
              <span>x</span>
            </div>
          </li>
          <li class="nav-item">
            <div class="chip">
              John Doe
              <span>x</span>
            </div>
          </li>
          <li class="nav-item">
            <div class="chip">
              John Doe
              <span>x</span>
            </div>
          </li>
          <li class="nav-item">See more</li>
        </ul>
      </div>
    </div>

    <div class="row" v-for="index in 10" :key="index">
      <div class="col-2">
        <img
          src="https://static-01.daraz.com.bd/p/b677601a70d4d080e1dfbc0b32d6e28e.jpg_340x340q80.jpg_.webp"
          width="=100px"
          height="100px"
        />
      </div>
      <div class="col-2">
        <h4>Justine due</h4>
        <p>London , UK 27 yrs old</p>
      </div>
      <div class="col-6">
        <ul class="nav justify-content-end">
          <li class="nav-item">
            <custom-button
              width="100px"
              height="30px"
              icon="caret-square-down"
              labelcolor="#fff"
              color=" green"
              radius="5px"
            >
              Shortlist
            </custom-button>
          </li>
          <li class="nav-item">
            <custom-button
              width="100px"
              height="30px"
              icon="caret-square-down"
              labelcolor="#fff"
              color=" cyan"
              radius="5px"
            >
              TeamList
            </custom-button>
          </li>
          <li class="nav-item">
                  <custom-button
              width="100px"
              height="30px"
              icon="caret-square-down"
              labelcolor="#fff"
              color=" blue"
              radius="5px"
            >
              connect
            </custom-button>
          </li>
          <li class="nav-item">
                   <custom-button
              width="100px"
              height="30px"
              icon="caret-square-down"
              labelcolor="#fff"
              color=" red"
              radius="5px"
            >
              block
            </custom-button>
          </li>
        </ul>
      </div>
      <div class="col-2">
        <custom-button
          width="200px"
          height="50px"
          labelcolor="#fff"
          color=" rgb(1, 3, 119)"
          radius="5px"
        >
          View Profile
        </custom-button>
      </div>
    </div>
  </div>
</template>

<script>
import CustomButton from "./ui/CustomButton.vue";
export default {
  components: { CustomButton },

  name: "content",

  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.chip {
  display: inline-block;
  padding: 0 21px;
  height: 27px;
  font-size: 16px;
  /* line-height: 29px; */
  border-radius: 25px;
  background-color: #b6aed5;
  margin: 2px;
}

.chip span {
  margin-left: 20px;
}
.filters {
  margin-bottom: 20px;
}
</style>
