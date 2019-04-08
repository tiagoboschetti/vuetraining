<template>
  <v-container>
    <div>
      <div class="texto">{{fafafa}}</div>
      <v-btn @click="mudarRola" class="sexo2">rola</v-btn>
      <v-btn @click="amostra">{{titulobotao}}</v-btn>
      <v-btn @click="incrementar" large icon>
        <v-icon large>add</v-icon>
      </v-btn>
    </div>
      <v-layout class="grey" wrap>
        <v-flex xs12 class="mb-3" red v-for="(x, index) in dados.menuitens" :key="index">
          <bunda-suja :esconder="false" @cancelar="cancelarPai" :cor="x.cor" :titulo="x.value" :text="x.onclick"></bunda-suja>
        </v-flex>
        <v-flex xs12> 
          <bunda-suja v-if="mostrarCard" :cor="cor1" :titulo="titulo1" :text="text1"></bunda-suja>
        </v-flex>
        <v-progress-circular size="100" v-model="valorbutao"></v-progress-circular>       
      </v-layout>
  </v-container>

</template>

<script>
import BundaSuja from './Button/index.vue';
import dados from './dataj.json';
import { setInterval } from 'timers';

  export default {
    components: {
      BundaSuja,
    },
    data: () => ({
      dados,
      rola: false,
      cor1: "pink",
      titulo1: "Dedé",
      text1: "apareceu?",
      mostrarCard: true,
      valorbutao: 0,
    }),
    computed: {
      fafafa() {
        return this.rola ? 'ROLA AZUL' : 'ROLA VERMELHA';
      },
      titulobotao() {
        return this.mostrarCard ? 'Esconder' : 'Mostrar';
      },
    },
    methods: {
      mudarRola() {
        this.rola = !this.rola;
      },
      cancelarPai() {
        console.log('Cancelou do Pai');
      },
      amostra() {
        this.mostrarCard = !this.mostrarCard;       
      },
      incrementar() {
        setInterval(() => {
          this.valorbutao += 25;
          if (this.valorbutao === 100) {
            this.valorbutao = 0
            };
        }, 500);
      }
    },
  };
</script>

<style lang="sass" scoped>
.sexo
  background: #122341
.sexo2
  background-color: #122341 !important
  color:  #122341 !important
.texto
  font-size: 3em
  font-weight: bold
</style>
