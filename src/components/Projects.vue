<template>
  <section class="project-section">
    <v-container>
      <v-row>
        <v-col>
          <h1>Projects</h1>
        </v-col>
      </v-row>
      <v-row class="justify-space-around mb-8 mt-4">
          <v-card 
          v-for="project in projects"
          :key="project.name" 
          class="" 
          max-width="300"
          >
            <v-img
              class="align-end"
              height="200px"
              :src="project.image"
            >
            </v-img>
             <v-card-title>{{project.name}}</v-card-title>

            <v-card-text class="text--primary">
              {{ truncate(project.description) }}
            </v-card-text>

            <v-card-actions>
              <v-btn color="orange" text :href="project.github">
                   Github Repo
                   </v-btn>

            </v-card-actions>
          </v-card>
      </v-row>
    </v-container>
  </section>
</template>

<script>


export default ({
    data() {
        return {
            projects: [
                {
                    name: 'Portfolio',
                    github: 'https://github.com/golfbauer/MyPortfolio',
                    description: 'Description Portfolio',
                    image: 'https://github.com/golfbauer/MyPortfolio/blob/master/src/profile.jpg?raw=true'
                },
                {
                    name: 'SH-Travel',
                    github: 'https://github.com/golfbauer/SH-Travel',
                    description: 'Description SH-Travel aaaaaaaaaaaaa aaaaaaaaaaaaaaaaaaaaaa aaaaaaaaaaaaaaa aaaaaaaaaaaaaaaaaaaaaaaa aaaaaaaaaaaaaaa aaaaaaaaaaaa',
                    image: 'https://github.com/golfbauer/SH-Travel/blob/main/src/frontend/src/assets/images/Luebeck_Login.jpg?raw=true'
                }
            ]
        }
    },
    methods: {
        truncate(str) { //For to long Description in card
            if(str.length > 80) {
                return str.slice(0, 79) + ' ...'
            }
            return str
        }
    }
})
</script>


<style scoped>
.project-section {
  background-color: #ffd563;
  
}
.v-image {
    border-bottom: 1px solid;
}
</style>