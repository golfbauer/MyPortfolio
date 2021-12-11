<template>
  <section id="projects" class="project-section">
    <v-container>
      <v-row>
        <v-col>
          <h1 style="font-size: 30px;">Projects</h1>
        </v-col>
      </v-row>
      <v-row class="justify-space-around mb-8 mt-4">
        <template v-for="(project, i) in projects">
          <v-col :key="i" cols="12" md="3">
            <v-hover v-slot="{ hover }">
              <v-card
                :key="project.name"
                :elevation="hover ? 12 : 2"
                :class="{ 'on-hover': hover }"
                class="d-flex flex-column"
                max-width="360"
                min-height="420"
              >
                <v-img class="align-end" height="200px" :src="project.image">
                </v-img>
                <v-card-title>{{ project.name }}</v-card-title>

                <v-card-text class="text--primary">
                  {{ truncate(project.description) }}
                </v-card-text>
                <v-spacer></v-spacer>
                <v-card-actions>
                  <v-btn color="orange" text :href="project.github">
                    Github Repo
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-hover>
          </v-col>
        </template>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: "SH-Travel",
          github: "https://github.com/golfbauer/SH-Travel",
          description:
            "In this project, 5 students and myself, worked in a scrum team to develop a responsive web application. I enjoyed the challenge, gained valuable experience, and was able to develop my skills particularly as a back-end developer.",
          image:
            "https://github.com/golfbauer/SH-Travel/blob/main/src/frontend/src/assets/images/Luebeck_Login.jpg?raw=true",
        },
        {
          name: "Function Analyzer",
          github:
            "https://github.com/golfbauer/FunctionAnalyzer/tree/main/components/src/main/java/de/hhn/it/pp/components/functionanalyzer",
          description:
            "This program takes in a function and computes its maxima, minima, intersection with y, x and so on. Though this project is 1 1/2 years old I am still very proud of what I accomplished.",
          image:
            "https://github.com/golfbauer/FunctionAnalyzer/blob/main/components/src/main/java/de/hhn/it/pp/components/functionanalyzer/FunctionAnalyzer.png?raw=true",
        },
        {
          name: "Schnek",
          github: "https://github.com/golfbauer/Schnek",
          description:
            "This project is part of a assignment for my 2D Game Engine Development module. I just started out with this project and it will be done until January.",
          image:
            "https://github.com/golfbauer/Schnek/blob/main/Games/Schnek/assets/images/SnakeByGoogle.png?raw=true",
        },
        {
          name: "Portfolio",
          github: "https://github.com/golfbauer/MyPortfolio",
          description:
            "Creating this Portfolio meant that it was my first time working with Gridsome and Vuetify. ",
          image:
            "https://github.com/golfbauer/MyPortfolio/blob/master/src/profile.jpg?raw=true",
        },
      ],
    };
  },
  methods: {
    truncate(str) {
      //For to long Description in card
      if (str.length > 150) {
        return str.slice(0, 149) + " ...";
      }
      return str;
    },
  },
};
</script>


<style scoped>
.project-section {
  background-color: #ffd563;
}
.v-image {
  border-bottom: 1px solid;
}
</style>