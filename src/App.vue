<template>
  <InputMessage
    v-for="post in posts"
    :key="post.id"
    :address="post.address"
  ></InputMessage>
</template>

<script>

import InputMessage from "./InputMessage.vue";
export default {
  components: {
    InputMessage,
  },
  data() {
    return {
      posts: [
        { id: 1, address: "http://www.SBliuyangqing.com" },          // <---地址写在这里
        { id: 2, address: "xxxx" },
        { id: 3, address: "xxxx" },
        { id: 4, address: "xxxx" },
        { id: 5, address: "xxxx" },
        { id: 6, address: "xxxx" },
        { id: 7, address: "xxxx" },
        { id: 8, address: "xxxx" },
      ],
    };
  },
};
</script>

<style scoped></style>
