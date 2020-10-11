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
        PROFESSIONAL SKILLS
      </div>
    </template>
    <div class="my-12">
      <template v-for="(item, index) in skills">
        <v-chip :key="index" label class="my-4" dark :color="item.color">
          {{ item.title }}
        </v-chip>
        <v-progress-linear
          :key="index"
          :color="item.color"
          height="10"
          :value="item.value"
          striped
        ></v-progress-linear>
        <br :key="index" />
      </template></div
  ></material-card>
</template>

<script>
export default {
  data: () => ({
    skills: [
      { value: '90', color: 'blue', title: 'HTML, CSS & Javascript' },

      {
        value: '100',
        color: 'light-green darken-4',
        title: 'VUE, VUEX & VUE-ROUTER',
      },

      {
        value: '80',
        color: 'lime darken-2',
        title: 'Server Side Render (NUXT JS)',
      },

      { value: '80', color: 'deep-orange', title: 'Git, CI, Deploy & G-Cloud' },

      { value: '90', color: 'deep-orange', title: 'Firebase' },

      { value: '80', color: 'purple', title: 'Scrum' },
    ],
  }),
}
</script>

<style></style>
