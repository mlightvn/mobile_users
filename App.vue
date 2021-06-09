<template>
  <view>
    <view class="header">
    </view>

    <Dialog />

    <UserList />

    <status-bar
        background-color="blue"
        bar-style="light-content"
    />

  </view>
</template>

<style>
.header{
  height: 20px;
  background-color: orange;
}
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
// import 'onsenui/css/onsenui.min.css'
// import 'onsenui/css/onsen-css-components.min.css'

import Dialog from "./views/common/Dialog.vue"
import UserList from "./views/users/Index.vue"


export default {
  components: {
    Dialog,
    UserList,
  },
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
