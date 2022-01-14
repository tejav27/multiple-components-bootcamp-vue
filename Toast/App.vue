<template>
  <div>
      <Toast v-for="color in colors" v-bind:key="color" v-bind:color="color" text="sucess"/>
      <Toast color="green" text="Successs"/>
      <Toast color="yellow" text="Warning!"/>
      <Toast color="red" text="Error!!!"/>
      <Toast color="blue" text="Information"/>
      <Toast color="teal" text="Processsingg"/>
  </div>
</template>

<script>
import Toast from './ToastComponent.vue'
export default {
    components:{ Toast },
    data(){return{
        colors:['red','yellow','blue','pink']
    }}

}
</script>

<style>

</style>