<template>
  <form action="" @submit="login">
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
export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    login(e) {
      // 폼 내의 값을 이용해 서버에 보낸다.
      // 폼의 기본동작 ==> 새로고침
      e.preventDefault(); // 폼 기본동작 막기
      console.log(this.username, this.password);
    },
  },
};
</script>

<style></style>
