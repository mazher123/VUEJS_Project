<template>
  <div class="container-fluid">
    <div class="row">
    <searchTab></searchTab>
    <Content></Content>
    </div>
  </div>
</template>

<script>
import searchTab from "../components/SearchTab.vue";
import Content from "../components/Content.vue";


export default {
  name: "homepage",
  components: {
    searchTab,
    Content,
  },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
