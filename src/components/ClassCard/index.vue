<template>
  <v-card class="charCard" ripple>
    <v-layout class="salsicha">
      <img class="classImage" :src="image"/>
      <div class="classImage__text">
        {{ title }}
      </div>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "oof! sorry"
    },
    image: {
      type: String,
      default:
        "https://66.media.tumblr.com/1ada0dd8dd359382129e11aa92e07939/tumblr_nn0yoz1ez31tv3g49o1_1280.jpg"
    }
  }
};
</script>

<style lang="sass">
.charCard
  width: 100%
  height: 100%
  transition: all .2s ease-in-out
  filter: grayscale(1)
  &:hover
    transform: scale(1.1)
    filter: grayscale(0)

.classImage
  display: flex
  height: 100%
  width: 100%
  justify-content: center
  transform: scaleX(1.04)
  &__text
    width: 100%
    height: 45%
    background: linear-gradient(to bottom, rgba(0,0,0,0), rgba(0,0,0,1))
    position: absolute
    display: flex
    justify-content: center
    align-items: flex-end
    font-size: 45px
    letter-spacing: 2px
    bottom: 0
.salsicha
  width: 100%
  height: 100%
</style>
