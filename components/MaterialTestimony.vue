<template>
  <v-card class="text-center v-card--testimony">
    <div class="pt-6">
      <v-icon color="yellow" x-large> mdi-format-quote-close </v-icon>
    </div>

    <v-card-text
      class="title font-weight-light white--text font-italic mb-3 col-md-8 mx-auto"
      v-text="blurb"
    />

    <div class="display-2 font-weight-light mb-2 ml-n6" v-text="author" />

    <div class="body-2 text-uppercase ml-n6" v-text="handle" />

    <v-avatar class="elevation-12" color="white" size="100">
      <v-img contain :alt="`${author} Testimonial`" :src="avatar" />
    </v-avatar>

    <div />
  </v-card>
</template>

<script>
export default {
  name: 'BaseMaterialTestimony',

  props: {
    author: {
      type: String,
      default: '',
    },
    avatar: {
      type: String,
      default:
        'https://demos.creative-tim.com/material-dashboard/assets/img/faces/card-profile1-square.jpg',
    },
    blurb: {
      type: String,
      default: '',
    },
    handle: {
      type: String,
      default: '',
    },
  },
}
</script>

<style lang="sass">
.v-card--testimony
  padding-bottom: 72px
  margin-bottom: 64px
  border-radius: 9px

  .v-avatar
    position: absolute
    left: calc(50% - 64px)
    top: calc(100% - 64px)
</style>
