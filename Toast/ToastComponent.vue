<template>
  <div>
    <h1 v-bind:style="{ color }">{{message}}</h1>
  </div>
</template>

<script>
export default {
  props:{
      text:{
          default:'Hellooo' 
      },
      color: String
  },
  data() {
    return {
      message:this.text
    };
  },
  mounted() {
    setTimeout(() => {
      this.message="";
      console.log("destroyed");
    }, 2000);
  },
};
</script>

<style>
</style>