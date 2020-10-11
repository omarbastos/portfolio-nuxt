<template>
  <v-carousel id="references">
    <v-carousel-item v-for="(item, index) in testimonies" :key="index">
      <material-testimony
        class="primary"
        :blurb="item.blurb"
        :author="item.author"
        :handle="item.handle"
        :avatar="item.avatar"
      />
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data: () => ({
    testimonies: [
      {
        blurb:
          'Really simple requirements gather, plenty of work examples to checkout before I committed. Would definitely hire again.',
        avatar: require('~/static/img/united-states.svg'),
        author: 'Xavian',
        handle: 'CarWallet',
      },
      {
        blurb:
          'Omar is the best frontend developer I have met on Fiverr. Very honest, has good work ethics, great communication. One of the best on Fiverr.',
        handle: 'Paperdaz',
        avatar: require('~/static/img/united-states.svg'),
        author: 'Mai',
      },
      {
        blurb: 'Great quality and fast delivery. Will order again',
        avatar: require('~/static/img/denmark.svg'),
        author: 'Mark Topper',
        handle: '@marktopper',
      },
      {
        blurb:
          "You are an amazing developer, the material design view is very beautiful. I'm surprised how quickly you work. Congratulations.",
        avatar: require('~/static/img/mexico.svg'),
        handle: 'Codecweb',
        author: 'Eduardo',
      },
      {
        blurb:
          'Really simple requirements gather, plenty of work examples to checkout before I committed. Would definitely hire again.',
        avatar: require('~/static/img/united-states.svg'),
        author: 'Remy',
        handle: 'Watermate',
      },
    ],
  }),
}
</script>

<style></style>
