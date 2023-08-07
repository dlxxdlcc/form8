<template>
  <form onsubmit="return false">
    <p>地址:</p>
    <input placeholder="edit me" type="text" v-model="message"/>
    <button @click="clickButton">click</button>
  </form>
</template>

<script>
import axios from "axios";
export default {
  props: ["address"],
  data() {
    return {
      message: "",
    };
  },
  methods: {
    clickButton() {
      console.log(this.message);
      axios({
        method: "post",
        url: this.address,
        headers: {
          "Content-Type": "multipart/form-data",
        },
        data: this.message,
      })
        .then((res) => {
          console.log(res);

        })
        .catch((err) => {
          console.log(err.response);
        });
        
    },
  },
};
</script>

<style></style>
