<template>
  <div>
      <h1>{{value}}</h1>
  </div>
</template>

<script>
export default {
    data(){return{
        value:'loading....'
    }},
 beforeMount(){
     this.showPreloader()
 },
 methods:{
     showPreloader(){
         setTimeout(()=>{this.value='successss'},2000)
     }
 }
}
</script>

<style>

</style>