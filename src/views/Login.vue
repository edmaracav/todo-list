<template>
    <div class="hero is-fullheight is-dark">
    <div class="hero-body">
      <div class="container has-text-centered">
        <div class="column is-8 is-offset-2">
          <h3 class="title has-text-white line typing-animation">TO-DO LIST</h3>
          <hr class="login-hr" />
          <p class="subtitle has-text-white">
            Faça login para criar suas listas!
          </p>
          <div class="box">
            <div class="title has-text-grey is-5">Insira seu login e senha</div>
            <form>
              <div class="field">
                <div class="control">
                  <p class="control has-icons-left has-icons-right">
                    <input class="input" type="email" placeholder="Email" v-model="form.email"/>
                    <span class="icon is-small is-left">
                      <i class="fas fa-envelope"></i>
                    </span>
                    <span class="icon is-small is-right">
                      <i class="fas fa-check"></i>
                    </span>
                  </p>
                </div>
              </div>
              <div class="field">
                <div class="control">
                  <p class="control has-icons-left">
                    <input
                      class="input"
                      type="password"
                      placeholder="Password"
                      v-model="form.password"
                    />
                    <span class="icon is-small is-left">
                      <i class="fas fa-lock"></i>
                    </span>
                  </p>
                </div>
              </div>
            </form>
            <label class="checkbox" style="margin: 20px">
              <input type="checkbox" />
              Lembrar login
            </label>
            <button class="button is-block is-danger is-fullwidth" @click="$router.push({ path: '/main' })">
              Login
            </button>
          </div>
          <p class="has-text-grey">
            <a class = "has-text-white" @click="$router.push({ path: '/cadastro' })">Fazer cadastro</a> &nbsp;·&nbsp;
            <a class = "has-text-white" @click="$router.push({ path: '/esquecisenha' })">Esqueci minha senha</a> &nbsp;·&nbsp;
            <a class = "has-text-white" href="">Precisa de ajuda?</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

export default class Login extends Vue {

 private form = {
        email: "",
        password: "",
    };

}

</script>


<style scoped>

.line{
  margin: 0 auto;
  white-space: nowrap;
  overflow: hidden;
  text-align: center;
  font-family: monospace;
  white-space: nowrap;
}

.typing-animation {
  animation: blinkCursor 500ms infinite normal, 
  typing 4s steps(50) 1s normal;
}
@keyframes typing{
  from{
    width: 0;
  }
  to{
    width:18em;
  }
}
@keyframes blinkCursor {
    from {
      border-right-color: rgba(2, 2, 2, 0.75);
    }
    to {
      border-right-color: transparent;
    }
  }
</style>