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
    <div class="my-8">
      <template v-for="(item, index) in skills">
        <div class="my-4" :key="index">
          <v-chip label class="my-4" dark :color="item.color">
            {{ item.title }}
          </v-chip>
          <v-progress-linear
            :color="item.color"
            height="10"
            :value="item.value"
            striped
          ></v-progress-linear>
        </div>
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
        title: 'Vue, Vuex & VueRouter',
      },

      {
        value: '80',
        color: 'lime darken-2',
        title: 'Server Side Render (NUXT JS)',
      },

      { value: '80', color: 'deep-orange', title: 'Git, CI, Deploy & G-Cloud' },

      { value: '90', color: 'deep-orange', title: 'Firebase' },

      { value: '80', color: 'purple', title: 'Scrum' },

      { value: '70', color: 'pink', title: 'Figma' },

      { value: '60', color: 'blue', title: 'TypeScript' },
    ],
  }),
}
</script>

<style></style>
