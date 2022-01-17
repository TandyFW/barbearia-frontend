<template>
  <main class="main">
    <form class="login-form">
      <div class="logo" />
      <div class="login-inputs">
        <Input placeholder="Digite seu e-mail" backLabel="Usuário" />
        <Input
          type="password"
          placeholder="Digite sua senha"
          backLabel="Senha"
        />
        <Button text="Entrar" type="button" id="btn-login" @click="logIn" />
      </div>
    </form>
  </main>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Input from "@/components/Input.vue";
import Button from "@/components/Button.vue";
import router from "@/router";

@Options({
  components: {
    Input,
    Button,
  },
  methods: {
    logIn: function () {
      router.push({ name: "Home" });
    },
  },
})
export default class Home extends Vue {}
</script>

<style scoped>
.main {
  background-image: url("../assets/barbearia-background.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.logo {
  border-radius: 50%;
  width: 50%;
  height: 50%;
  background-image: url("../assets/logo.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.login-form {
  background-color: rgba(0, 0, 0, 0.3);
  width: 50%;
  height: 60%;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
.login-inputs {
  display: flex;
  flex-direction: column;
  width: 50%;
}
</style>
