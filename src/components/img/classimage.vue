<template>
  <v-card :color="cor">
    <v-card-title>
      {{titulo}}
    </v-card-title>
    <v-card-text>
      {{text}}
    </v-card-text>
    <v-card-actions>
      <v-layout>
        <v-btn @click="cancelar">Cancelar</v-btn>
        <v-btn v-if="esconder" @click="confirmar">Confirmar</v-btn>
      </v-layout>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    titulo: {
      type: String,
      default: '',
    },
    esconder: {
      type: Boolean,
      default: true,
    },
    text: {
      type: String,
      default: '',
    },
    cor: {
      type: String,
    },
  },

  methods: {
    cancelar() {
      this.$emit('cancelar');
    },
    confirmar() {
      this.$emit('confirmar');
    },
  },
};
</script>

