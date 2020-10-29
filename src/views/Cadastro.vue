<template>
<CadastroComponent></CadastroComponent>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import CadastroComponent from '@/components/CadastroComponent.vue'; // @ is an alias to /src

@Options({
  components: {
    CadastroComponent,
  },
})
export default class Cadastro extends Vue {}

</script>
