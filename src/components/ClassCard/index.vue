<template>
  <v-card class="charCard mx-3" ripple>
    <v-card-text class="pa-0">
      <v-layout justify-center align-center>
        <img class="classImage" :src="image" height="720px" />
        <div class="classImage__text">
          {{ title }}
        </div>
      </v-layout>
    </v-card-text>
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
.v-card
  border-radius: 20px 20px 20px 20px !important
.charCard
  transition: all .2s ease-in-out
  filter: grayscale(1)
  &:hover
    transform: scale(1.1)
    filter: grayscale(0)

.classImage
  display: flex
  border-radius: 20px 20px 20px 20px !important
  justify-content: center
  transform: scaleX(1.04)
  &__text
    width: 100%
    height: 45%
    border-radius: 20px 20px 20px 20px !important
    background: linear-gradient(to bottom, rgba(0,0,0,0), rgba(0,0,0,1))
    position: absolute
    display: flex
    justify-content: center
    align-items: flex-end
    font-size: 45px
    letter-spacing: 2px
    bottom: 0px
</style>
