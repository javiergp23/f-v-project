<script setup>
export default {
  data (){
    return{
      productos:[],
    }
  },
  async function name(params) {
    
  }
},

</script>

<template>
  <div>
    <h1>Mis productos</h1>
    <ul>
      <li  v-for="producto in productos" :key="producto.id">
        {{producto}}
      </li>
    </ul>
  </div>
</template>

<style>

</style>
