<template>
  <v-container id="about">
    <v-card elevation="6" tile>
      <v-card-text>
        <v-row>
          <v-col justify="center" align="center" cols="12" md="6"
            ><v-img
              class="my-auto"
              style="border-radius: 9px"
              max-width="300"
              height="100%"
              src="img/profile.png"
            ></v-img
          ></v-col>
          <v-col cols="12" md="6">
            <v-chip large class="mb-4" label color="primary">
              Hello! &#x1F44B;</v-chip
            >
            <h2 class="font-weight-light">
              I'm
              <span class="font-weight-bold black--text"
                >Omar Jesus Hernandez Bastos</span
              >
            </h2>
            <h3 class="font-weight-medium">
              Web Developer and Electronic Engineer
            </h3>
            <v-divider class="my-4"></v-divider>
            <v-simple-table>
              <template v-slot:default>
                <tbody>
                  <tr v-for="(item, index) in mainTable" :key="index">
                    <td class="font-weight-bold">{{ item.key }}</td>
                    <td>{{ item.value }}</td>
                  </tr>
                </tbody>
              </template>
            </v-simple-table>
          </v-col></v-row
        ></v-card-text
      ><v-card-actions class="primary">
        <v-spacer></v-spacer>
        <v-btn
          :x-large="$vuetify.breakpoint.mdAndUp"
          icon
          dark
          target="_blank"
          href="https://github.com/omarbastos/"
          ><v-icon>mdi-github</v-icon></v-btn
        >
        <v-btn
          :x-large="$vuetify.breakpoint.mdAndUp"
          icon
          dark
          href="mailto:omarsro@gmail.com?subject='Hello'"
          ><v-icon>mdi-email</v-icon></v-btn
        >
        <v-btn
          :x-large="$vuetify.breakpoint.mdAndUp"
          icon
          dark
          target="_blank"
          href="https://www.linkedin.com/in/omar-bastos/"
          ><v-icon>mdi-linkedin</v-icon></v-btn
        >
        <v-btn
          :x-large="$vuetify.breakpoint.mdAndUp"
          icon
          dark
          href="tel:+584147233668"
          ><v-icon>mdi-phone</v-icon></v-btn
        >

        <v-spacer></v-spacer>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    mainTable: [
      { key: 'AGE', value: '27' },
      { key: 'ADDRESS', value: 'San Cristobal,Tachira, Venezuela' },
      { key: 'E-MAIL', value: 'omarsro@gmail.com' },
      { key: 'PHONE', value: '+58 414 723 3668' },
      { key: 'FREELANCE', value: 'till January, 2018' },
    ],
  }),
}
</script>

<style></style>
