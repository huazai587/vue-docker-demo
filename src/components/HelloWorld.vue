<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>

import axios from 'axios';
export default {
  props: {
    msg: String 
  },


  created (){
    axios.get('/api/json',{
      params:{}
  }).then(
    res => {
     console.log(res)
    }
  ).catch(
    error => {
      console.log(error)
    }
  )}
}
</script>


