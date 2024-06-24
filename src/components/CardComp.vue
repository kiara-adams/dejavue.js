<template>
    <div class="card" :style="{ borderColor: gender === 'ale'? 'gold' : 'green' }">
      <slot name="header"></slot>
      <slot name="content"></slot>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      gender: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style>
  .card {
    border: 1px solid;
    padding: 10px;
    margin: 10px;
  }
  </style>
