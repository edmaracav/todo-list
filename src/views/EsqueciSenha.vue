<template>
  <div class="hero is-fullheight is-dark">
    <div class="hero-body">
      <div class="container has-text-centered">
        <div class="column is-8 is-offset-2">
          <h3 class="title has-text-white line typing-animation">Esqueci minha senha</h3>
          <hr class="login-hr" />
          <div class="box">
            <div class="title has-text-grey is-5">Insira seu email para redefinição da senha</div>
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
            </form>
          </div>
          <button class="button is-block is-danger is-fullwidth">
            Enviar
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';


export default class EsqueciSenha extends Vue {
     private form = {
        email: ""
    };
}

</script>
