<template>
  <v-carousel
    height="auto"
    id="references"
    hide-delimiter-background
    hide-delimiters
    show-arrows-on-hover
  >
    <v-carousel-item v-for="(item, index) in testimonies" :key="index">
      <v-container>
        <material-testimony
          class="primary"
          :blurb="item.blurb"
          :author="item.author"
          :handle="item.handle"
          :avatar="item.avatar"
      /></v-container>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data: () => ({
    testimonies: [
      {
        blurb:
          "Omar is a person that not only asks what is the task, but that is the problem to give you the solution you need, even when you don't know you need it. He is highly motivated to do quality work, he's detailed oriented and meets his deadlines. I will gladly continue to work with him.",
        avatar: require('~/static/img/germany.svg'),
        author: 'Gustavo',
        handle: 'GM at Metax Technologie',
      },
      {
        blurb:
          'It was excellent working with Omar. He guided us throughout the project process. If you have no experience or knowledge of development, I highly recommend Omar. His way of explaining and teaching is precious. He has excellent emotional intelligence and offers practical and straightforward solutions to complicated problems.',
        avatar: require('~/static/img/united-states.svg'),
        author: 'Xavian',
        handle: 'Co-Founder of CarWallet',
      },
      {
        blurb:
          'Omar is the best frontend developer I have met on Fiverr. Very honest, has good work ethics, great communication. One of the best on Fiverr.',
        handle: 'CEO of Paperdaz',
        avatar: require('~/static/img/united-states.svg'),
        author: 'Mai',
      },
      {
        blurb: 'Great quality and fast delivery. Will order again',
        avatar: require('~/static/img/denmark.svg'),
        author: 'Mark Topper',
        handle: 'CEO of @ulties.',
      },
      {
        blurb:
          "You are an amazing developer, the material design view is very beautiful. I'm surprised how quickly you work. Congratulations.",
        avatar: require('~/static/img/mexico.svg'),
        handle: 'CEO of Codecweb',
        author: 'Eduardo',
      },
      {
        blurb:
          'Really simple requirements gather, plenty of work examples to checkout before I committed. Would definitely hire again.',
        avatar: require('~/static/img/united-states.svg'),
        author: 'Remy',
        handle: 'CEO of Watermate',
      },
    ],
  }),
}
</script>

<style></style>
