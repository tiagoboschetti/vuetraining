<template>
  <v-container fluid>
    <v-layout
      justify-center
      align-center
    >
    <v-app dark>
      <v-img
        src="https://i.pinimg.com/originals/34/48/a0/3448a03ae321d27362bee79748e8c859.jpg"
        gradient="to top, rgba(20,20,0,.9), rgba(20,20,0,.7)"
      ></v-img>
          <v-flex text-xs-center>
              <v-card class="elevation-24" height="500px" width="800px">
            </v-card>
          </v-flex>
      </v-app>
    </v-layout>
  </v-container>
  <!--
  <v-container>
    <div>
      <div class="texto">{{fafafa}}</div>
      <v-btn @click="mudarRola" class="sexo2">rola</v-btn>
      <v-btn @click="amostra">{{titulobotao}}</v-btn>
      <v-btn @click="incrementar" large icon>
        <v-icon large>add</v-icon>
      </v-btn
    </div>
      <v-layout class="bg" wrap>
        <v-flex xs12 class="mb-3" red v-for="(x, index) in dados.menuitens" :key="index">
          <bunda-suja :esconder="false" @cancelar="cancelarPai" :cor="x.cor" :titulo="x.value" :text="x.onclick"></bunda-suja>
        </v-flex>
        <v-flex xs12>
          <bunda-suja v-if="mostrarCard" :cor="cor1" :titulo="titulo1" :text="text1"></bunda-suja>
        </v-flex>
        <v-progress-circular size="100" v-model="valorbutao"></v-progress-circular>
      </v-layout>
  </v-container>
  -->
</template>

<script>
  export default {
  }
</script>

<style lang="sass" scoped>

</style>
