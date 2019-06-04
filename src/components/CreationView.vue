<template>
  <v-app dark>
    <div class="bgImage">
      <div class="bgImage__overlay" />
      <div class="bgImage__content">
        <v-card
          class="elevation-24"
          color="grey darken-4"
        >
          <v-layout class="rola">
            <v-card-text class="foo">
              <v-flex
                xs12
                sm6
                lg3
                class="mb-3"
                v-for="classes in classesData"
                :key="classes.title"
              >
                <class-card :title="classes.title" :image="classes.image"/>
              </v-flex>
            </v-card-text>
          </v-layout>
        </v-card>
      </div>
    </div>
  </v-app>
  <!--
  <v-container>
    <div>
      <div class="texto">{{fafafa}}</div>
      <v-btn @click="mudarRola" class="sexo2">rola</v-btn>
      <v-btn @click="amostra">{{titlebotao}}</v-btn>
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
import ClassCard from "./ClassCard";
import classesData from "./json/classesData.json";

export default {
  components: {
    ClassCard,
    // classesData,
  },
  computed: {
    classesData() {
      return classesData.data;
    }
  },
};
</script>

<style lang="sass" scoped>
.bgImage
  display: flex
  justify-content: center
  background-image: url('https://i.pinimg.com/originals/34/48/a0/3448a03ae321d27362bee79748e8c859.jpg')
  height: 100vh
  &__overlay
    background:  linear-gradient(to bottom, rgba(20,0,0,0.7), rgba(20,0,0,0.9))
    height: 100vh
    width: 100vw
  &__content
    position: absolute
    display: flex
    justify-content: center
    align-items: center
    height: 100%
    width: 85%
.rola
  background-color: red !important
  height: 100%
  display: flex
  align-items: center
  justify-content: center
.foo
  display: flex
  justify-content: space-between
</style>
