<template>
  <material-card
    id="skills"
    icon="mdi-code-tags-check"
    color="primary"
    elevation="6"
    inline
    class="px-5 py-3"
  >
    <template v-slot:after-heading>
      <div class="title text-no-wrap font-weight-bold primary--text">
        Professional Skills
      </div>
    </template>
    <div>
      <v-chip label class="mb-2" dark color="blue">
        HTML, CSS & Javascript
      </v-chip>
      <v-progress-linear
        color="blue"
        height="10"
        value="90"
        striped
      ></v-progress-linear>
      <br />
      <v-chip label class="mb-2" dark color="light-green darken-4">
        VUE JS
      </v-chip>
      <v-progress-linear
        color="light-green darken-4"
        height="10"
        value="100"
        striped
      ></v-progress-linear>
      <br />
      <v-chip label class="mb-2" dark color="lime darken-2">
        Server Side Render (NUXT JS)
      </v-chip>
      <v-progress-linear
        color="lime darken-2"
        height="10"
        value="80"
        striped
      ></v-progress-linear>
      <br />
      <v-chip label class="mb-2" dark color="deep-orange">
        Git, CI & Deploy
      </v-chip>
      <v-progress-linear
        color="deep-orange"
        height="10"
        value="80"
        striped
      ></v-progress-linear>
      <br />
      <v-chip label class="mb-2" dark color="red"> Firebase </v-chip>
      <v-progress-linear
        color="red"
        height="10"
        value="90"
        striped
      ></v-progress-linear>
      <br />
      <v-chip label class="mb-2" dark color="grey darken-2"> Node </v-chip>
      <v-progress-linear
        color="grey darken-2"
        height="10"
        value="70"
        striped
      ></v-progress-linear>
      <br />
      <v-chip label class="mb-2" dark color="purple"> SCRUM </v-chip>
      <v-progress-linear
        color="purple"
        height="10"
        value="90"
        striped
      ></v-progress-linear
      ><br /></div
  ></material-card>
</template>

<script>
export default {}
</script>

<style></style>
