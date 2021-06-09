<template>
  <view class="container">
    <text class="text-color-primary">{{message}}</text>
    <button title="Press me!" @press="exclaim" />
  </view>
</template>

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

<script>

export default {
  data() {
    return {
      name: "MLight",
      message: "Hello World",
    };
  },
  methods: {
    exclaim() {
      this.message += "!";
    }
  },
}
</script>
