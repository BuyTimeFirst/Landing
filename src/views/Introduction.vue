<template>
  <v-app>
    <v-main id="main-view">
        <!-- Parallax -->
        <v-row
                align="center"
        >
            <v-parallax id="parallax" src="https://cdn.vuetifyjs.com/images/parallax/material.jpg">
                <v-row
                        align="center"
                        justify="center"
                >
                    <v-col class="text-center" cols="12">
                        <h1 class="display-1 font-weight-thin mb-4">Buy your time first</h1>
                        <h4 class="subheading">Before anything else</h4>
                    </v-col>
                </v-row>
            </v-parallax>
        </v-row>
        <!-- Parallax -->

        <!-- About the company -->
        <v-row
                align="center"
                justify="center"
        >
            <v-col class="text-center" cols="12">
                <h1 class="display-1 font-weight-thin mb-4">What is this?</h1>
                <h4 class="subheading">asdf</h4>
            </v-col>
        </v-row>
        <!-- About -->

        <!-- Card Rows-->
                <v-row dense>
                    <v-col
                            v-for="card in cards"
                            :key="card.title"
                            :cols="card.flex"
                    >
                        <v-card>
                            <v-img
                                    :src="card.src"
                                    class="white--text align-end"
                                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                                    height="200px"
                            >
                                <v-card-title v-text="card.title"></v-card-title>
                            </v-img>

                            <v-card-actions>
                                <v-spacer></v-spacer>

                                <v-btn icon>
                                    <v-icon>mdi-heart</v-icon>
                                </v-btn>

                                <v-btn icon>
                                    <v-icon>mdi-bookmark</v-icon>
                                </v-btn>

                                <v-btn icon>
                                    <v-icon>mdi-share-variant</v-icon>
                                </v-btn>
                            </v-card-actions>
                        </v-card>
                    </v-col>
                </v-row>
        <!-- /Card Rows-->
    </v-main>
    <v-footer
            color="indigo"
            app
    >
      <span class="white--text">&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<style scoped>
   #main-view {
       padding: 0 !important;
   }

   #parallax {
       width: 100%;
       height: 100%;
   }
</style>

<script>
  export default {
    props: {
      source: String,
    },
    data: () => ({
      drawer: null,
      cards: [
        { title: 'Deal', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6 },
        { title: 'Deal 2', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6 },
        { title: 'Deal 3', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6 },
        { title: 'Deal 4', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6 },
      ],
    }),
  }
</script>