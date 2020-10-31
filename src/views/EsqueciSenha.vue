<template>
<EsqueciSenhaComponent></EsqueciSenhaComponent>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import EsqueciSenhaComponent from '@/components/EsqueciSenhaComponent.vue'; // @ is an alias to /src

@Options({
  components: {
    EsqueciSenhaComponent,
  },
})
export default class EsqueciSenha extends Vue {}

</script>
