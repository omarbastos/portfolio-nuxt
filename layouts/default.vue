<template>
  <v-app app>
    <v-app-bar fixed app color="white" class="primary--text">
      <v-img
        @click="$vuetify.goTo('#about', options)"
        class="mx-2"
        src="img/obicon-sin-fondo.svg"
        max-height="56"
        max-width="56"
        contain
      ></v-img>
      <v-toolbar-title class="font-weight-bold">OmarBastos.dev</v-toolbar-title>
      <v-spacer />
      <template v-if="$vuetify.breakpoint.mdAndUp">
        <v-btn
          text
          class="primary--text"
          @click="$vuetify.goTo('#about', options)"
        >
          ABOUT
        </v-btn>
        <v-btn
          text
          class="primary--text"
          @click="$vuetify.goTo('#skills', options)"
        >
          SKILLS
        </v-btn>
        <v-btn
          text
          class="primary--text"
          @click="$vuetify.goTo('#experiences', options)"
        >
          EXPERIENCE
        </v-btn>
        <v-btn
          text
          class="primary--text"
          @click="$vuetify.goTo('#references', options)"
        >
          REFERENCES
        </v-btn>
      </template>

      <v-menu offset-y v-else>
        <template v-slot:activator="{ on }">
          <v-btn
            aria-label="menu"
            color="primary"
            class="hidden-sm-and-up"
            icon
            v-on="on"
          >
            <v-icon>mdi-menu</v-icon>
          </v-btn>
        </template>
        <v-list>
          <v-list-item @click="$vuetify.goTo('#about', options)">
            <v-list-item-title class="d-flex align-center"
              >ABOUT</v-list-item-title
            >
          </v-list-item>
          <v-list-item @click="$vuetify.goTo('#skills', options)">
            <v-list-item-title class="d-flex align-center"
              >SKILLS</v-list-item-title
            >
          </v-list-item>
          <v-list-item @click="$vuetify.goTo('#experiences', options)">
            <v-list-item-title class="d-flex align-center"
              >EXPERIENCE</v-list-item-title
            >
          </v-list-item>
          <v-list-item @click="$vuetify.goTo('#references', options)">
            <v-list-item-title class="d-flex align-center"
              >REFERENCES</v-list-item-title
            >
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
    <VueScrollProgress></VueScrollProgress>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

    <v-footer :absolute="!fixed" app>
      <v-spacer></v-spacer>
      <span>&copy; {{ new Date().getFullYear() }} omarbastos.dev</span>
      <v-spacer></v-spacer>
    </v-footer>
  </v-app>
</template>

<script>
import * as easings from 'vuetify/es5/services/goto/easing-patterns'
export default {
  data() {
    return {
      options: {
        easing: 'easeInOutCubic',
      },
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>
<style>
/* play with some lines below */
#progress-container-el {
  /* background */
  background-color: #f4f4f4 !important;
}

#progress-el {
  /* progress bar */
  background-color: #0d47a1 !important;
}
</style>
