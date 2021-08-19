<template>
  <div id="app">
    <v-app id="inspire">
      <v-card flat>
        <v-container>
          <v-row>
            <v-col md="4">
              <div>
                <v-toolbar dense color="grey lighten-3" class="rounded-xl">
                  <v-btn icon class="hidden-xs-only">
                    <v-icon>mdi-magnify</v-icon>
                  </v-btn>
                  <v-toolbar-title
                    class="grey lighten-3 deep-orange accent-4--text"
                    >Search Anything...</v-toolbar-title
                  >
                  <v-spacer></v-spacer>
                </v-toolbar>
              </div>
            </v-col>

            <v-col md="4" class="ml-auto text-right">
              <v-card class="pa-2" flat >
                <v-icon large color="green darken-2" class="mr-8">
                  mdi-bell
                </v-icon>
                      <v-avatar>
        <img
          src="https://cdn.vuetifyjs.com/images/john.jpg"
          alt="John"
        >
      </v-avatar>
              </v-card>
            </v-col>
          </v-row>

          

          <v-container>
            <div class="Gallery">Gallery</div>
          </v-container>

          <v-row dense>
            <v-col v-for="n in 12" :key="n" class="d-flex child-flex" cols="3">
              <v-card class="rounded-xl">
                
                <v-img
                  :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                  :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                  aspect-ratio="1"
                  class="grey lighten-2 align-end"
                >
                  <v-row>
                    <v-col cols="12">
                      <v-card-title class="product white--text"
                        >Buff/Sukuti</v-card-title
                      >
                      <v-card-actions>
                        <v-chip class="grey darken-1 white--text">
                          PUBLISHED
                        </v-chip>
                        <v-spacer></v-spacer>
                        <v-spacer></v-spacer>
                        <v-btn icon>
                          <v-icon size="35" color="white"
                            >mdi-dots-horizontal</v-icon
                          >
                        </v-btn>
                      </v-card-actions>
                    </v-col>
                  </v-row>
                </v-img>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-app>
  </div>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    //
  }),
};
</script>
<style>
.productbtns {
  margin: 0;
  padding: 0;
}

.product {
  margin: 0;
  padding: 0;
}
.Gallery {
  font-size: 40px;
  font-weight: 600;
}
</style>
