<template>
  <v-app class="white work">
    <v-container class="pa-0 mb-3">
      <v-layout
        text-center
        wrap
      >
        <v-flex xs11 style="margin-top: 100px; padding-top: 70px; text-align: left; margin-bottom: 60px;">
          <h1 class="display-2 font-weight-light mb-3">
            What I've <span style="color: #580aff;">built</span>.
          </h1>
          <p class="font-weight-light mb-1" style="font-size: 20px;">
            {{ workJson.projectsContent }}
          </p>
        </v-flex>
      </v-layout>

      <v-layout
        text-center
        wrap
        row
        style="margin-bottom: 80px;"
      >
        <v-flex xs12 sm6 md4 lg4  xs6 v-for="(item, i) in workJson" :key="i" style="text-align: left;" :id="item.id">
          <v-list two-line subheader>
            <v-list-item>
              <v-list-item-avatar>
                <v-icon class='grey lighten-1 white--text'>
                  {{ i | getIcon }}
                </v-icon>
              </v-list-item-avatar>

              <v-list-item-content>
              <v-list-item-title v-text="item.title"></v-list-item-title>
                <v-list-item-subtitle v-text="item.shortDescription"></v-list-item-subtitle>
              </v-list-item-content>

              <v-list-item-action>
                <v-btn icon :href="item.links[0].link">
                  <v-icon color="grey lighten-1">mdi-information</v-icon>
                </v-btn>
              </v-list-item-action>
              
            </v-list-item>
          </v-list>

        </v-flex>
      </v-layout>

    </v-container>
  </v-app>
</template>

<script>
import workDataJson from "../../assets/data/work.json";
export default{
  data(){
    return {
      workJson: workDataJson["portfolioItems"]
    }
  },
  filters: {
    getIcon: (index) => {
      return "P"+index
    }
  }
}
</script>
