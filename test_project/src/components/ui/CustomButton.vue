<template>
  <div class="counter">
    <button  :style="{
      
      width:width,
      height:height,
      backgroundColor: color,
      color:labelcolor,
      borderRadius:radius,
     

      }" >
      <span > <font-awesome-icon class="arrow-icon" :icon="icon" /></span>
      <slot></slot>
    </button>
  </div>
</template>

<script>
export default {
  props: {
    width: String,
    height: String,
    color: String,
    icon: String,
    labelcolor:String,
    radius:String
  },
  data(){

    return{
      
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.counter {
  display: inline-block;
}</style>
