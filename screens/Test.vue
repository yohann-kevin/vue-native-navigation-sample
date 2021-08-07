<template>
  <view class="container">
    <!-- <header/> -->
    <text>{{ welcomeMsg }}</text>
    <button v-bind:title="message" v-bind:on-press="displayMessage"/>
    <text>{{ dynamicMessage }}</text>
    <button v-bind:title="btnCounterMsg" v-bind:on-press="counting" />
    <text>{{ counterMessage }}{{ counter }}</text>
  </view>
</template>

<script>
export default {
  data: function() {
    return {
      welcomeMsg: "Welcome to my vue-native app",
      message: "Hello World",
      dynamicMessage: "",
      btnCounterMsg: "press for increments counter",
      counterMessage: "Counter : ",
      counter: 0
    };
  },
  methods: {
    displayMessage: function() {
      this.dynamicMessage = "Hello World !";
    },
    counting: function() {
      this.counter++;
      console.log("plop");
    }
  }
};
</script>

<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>