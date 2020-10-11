<template>
  <v-timeline align-top dense class="my-12" id="experiences">
    <v-timeline-item
      v-for="(timeline, i) in timelines"
      :key="i"
      :color="timeline.color"
      :icon="timeline.icon"
      fill-dot
      large
    >
      <v-card class="pa-6">
        <v-chip :color="timeline.color" class="overline mb-3" small>
          {{ timeline.chip }}
        </v-chip>

        <p class="subtitle-1" v-text="timeline.text" />

        <div class="text-uppercase body-2" v-text="timeline.subtext" />

        <template v-if="timeline.action">
          <v-divider class="mb-3" />

          <v-menu
            v-model="menu"
            bottom
            offset-y
            origin="top left"
            right
            transition="scale-transition"
          >
            <template v-slot:activator="{ attrs, on }">
              <v-btn
                v-bind="attrs"
                :color="timeline.action"
                default
                rounded
                v-on="on"
              >
                <v-icon left v-text="timeline.actionIcon" />
                <v-icon right>
                  {{ menu ? 'mdi-menu-up' : 'mdi-menu-down' }}
                </v-icon>
              </v-btn>
            </template>

            <v-sheet>
              <v-list>
                <v-list-item v-for="a in timeline.actions" :key="a" link>
                  <v-list-item-title v-text="a" />
                </v-list-item>
              </v-list>
            </v-sheet>
          </v-menu>
        </template>
      </v-card>
    </v-timeline-item>
  </v-timeline>
</template>

<script>
export default {
  data: () => ({
    timelines: [
      {
        chip: 'Freelancer',
        color: 'success',
        icon: 'mdi-briefcase',
        text:
          'This was beginning of my career. I was responsible for working on a range of projects, designing appealing websites and interacting on a daily basis with graphic designers, back-end developers and marketers.',
        subtext: '2015-2018',
      },
      {
        chip: 'A.B.A.E.',
        color: 'error',
        icon: 'mdi-satellite-variant',
        text:
          'I worked as part of the government institution in charge of the space administration of Venezuela (ABAE), carrying out a project of a prototype of a fishing boat monitoring system as requested by the Research and Development Manager. This was part of my degree project to receive my electronic engineering degree.',
        subtext: 'Jan 2019- Jul 2019',
      },
      {
        chip: 'Electronic Engineer Graduate',
        color: 'primary',
        icon: 'mdi-school',
        text:
          'Graduated as the first of my class, in Electronic Engineering at the National Experimental University of Tachira (UNET)',
      },
      {
        chip: 'Fix4u Solutions',
        color: 'info',
        icon: 'mdi-laptop',
        text:
          'Fix4u is a startup dedicated to outsourced services, in which I carried out different tasks such as design, development and creation of websites and web applications. I had the privilege of learning how to work directly with clients and coordinate projects, successfully accomplishing more than 16 projects in approximately 10 months.',
        subtext: 'Jul 2019 - March 2020',
      },
      {
        chip: 'Freelancer',
        color: 'info',
        icon: 'mdi-code-tags',
        text:
          'I have done projects as a freelance, such as developing web pages, application demos, proofs of concept, complete app, app for desktop & Android and the Progressive Web Application (PWA)',
        subtext: 'March 2020 - Jul 2020',
      },
      {
        chip: 'CarWallet.io',
        color: 'success',
        icon: 'mdi-car',
        text:
          'This was a project for a Progressive Web Application, in which I worked as a web developer both in the frontend (home page, main application and administrative panel) and in the development of the backend with Firebase, it was a great challenge but with a great result and total customer satisfaction, an unforgettable experience that helped me grow a lot. It was a part time job.',
        subtext: 'Jun 2020 - Sept 2020',
      },
      {
        chip: 'Metax Technologie',
        color: 'error',
        icon: 'mdi-dev-to',
        text:
          'At Metax Technologie, I am responsible for developing a PWA (Progressive Web Application) for maintenance and reliability in the industry. Together with the work team, I carry out the development of the Backend and Frontend, providing solutions to the pre-established requirements.',
        subtext: 'Jun 2020 - Present',
      },
    ],
  }),
}
</script>

<style></style>
