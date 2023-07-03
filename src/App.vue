<template>
  <form action="" @submit.prevent="login">
    <section>
      <label for="userid">아이디</label>
      <input id="userid" type="text" v-model="username" />
    </section>
    <section>
      <label for="password">비밀번호</label>
      <input id="password" type="password" v-model="password" />
    </section>
    <button>login</button>
  </form>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    login() {
      // 폼 내의 값을 이용해 서버에 보낸다.
      // 폼의 기본동작 ==> 새로고침
      // e.preventDefault(); // 폼 기본동작 막기 => 자바스크립트 방식
      console.log(this.username, this.password);
      const url = "https://jsonplaceholder.typicode.com/users";
      const data = {
        username: this.username,
        password: this.password,
      };
      axios
        .post(url, data)
        .then(response => {
          console.log(response);
        })
        .catch(error => {
          console.log(error);
        });
    },
  },
};
</script>

<style></style>
