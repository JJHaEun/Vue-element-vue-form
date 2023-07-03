<template>
  <form action="">
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
};
</script>

<style></style>
