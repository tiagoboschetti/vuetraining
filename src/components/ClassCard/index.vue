<template>
  <v-card class="charCard mx-3" ripple>
    <v-card-text class="pa-0">
      <v-layout justify-center align-center>
        <img class="classImage" :src="image" height="720px" />
        <div class="classImage__text">
          {{ titulo }}
        </div>
      </v-layout>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    titulo: {
      type: String,
      default: "oof! sorry"
    },
    image: {
      type: String,
      default: "http://pngimg.com/uploads/alien/alien_PNG98.png"
    }
  }
};
</script>

<style lang="sass">
.charCard
  transition: all .2s ease-in-out
  filter: grayscale(1)
  &:hover
    transform: scale(1.1)
    filter: grayscale(0)

.classImage
  display: flex
  justify-content: center
  transform: scaleY(-1)
  &__text
    width: 100%
    height: 45%
    background:  linear-gradient(to bottom, rgba(0,0,0,0), rgba(0,0,0,1))
    position: absolute
    display: flex
    justify-content: center
    align-items: flex-end
    font-size: 45px
    letter-spacing: 2px
    bottom: 0px
</style>
