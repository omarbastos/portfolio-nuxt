<template>
  <v-container>
    <about></about>
    <div class="my-12 d-flex justify-center align-center">
      <v-btn
        :x-large="$vuetify.breakpoint.mdAndUp"
        color="black"
        target="_blank"
        href="/resume.pdf"
        outlined
        >Download Resume</v-btn
      >
    </div>
    <p class="my-12 headline text-center col-md-10 mx-auto">
      Electronic Engineer and Senior Web Developer specialized in front-end
      development. Experience in all phases of the development cycle of dynamic
      web projects. Well versed in numerous programming languages, including
      JavaScript, Python, Flutter, and embedded systems, with the innate ability
      to learn and master new technologies.
    </p>
    <skills></skills>
    <experience></experience>
    <references></references>
  </v-container>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
export default {
  components: {
    Logo,
    VuetifyLogo,
  },
}
</script>
