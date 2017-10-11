<template lang="html">
  <div>
    <div id="on" @click="switched(true)" :class="{active: value}">ON</div>

    <div id="off" @click="switched(false)" :class="{active: !value}">OFF</div>
  </div>
</template>

<script>
  export default {
    props: ['value'],
    methods: {
      switched (isOn) {
        this.$emit('input', isOn);
      },
    },
  };
</script>

<style lang="css">
  #on, #off {
    width: 40px;
    height: 20px;
    background-color: #aaa;
    padding: 2px;
    display: inline-block;
    margin: 10px -2px;
    box-sizing: content-box;
    cursor: pointer;
    text-align: center;
    border: 2px solid black;
    font-weight: bold;
  }

  #on:hover{
    background-color: lightgreen;
  }

  #on.active {
    background-color: lime;
  }

  #off:hover {
    background-color: lightcoral;
  }

  #off.active {
    background-color: red;
  }
</style>
