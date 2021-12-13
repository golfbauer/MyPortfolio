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
                min-height="500"
              >
                <v-img class="align-end" height="200px" :src="project.image">
                </v-img>
                <v-card-title>{{ project.name }}</v-card-title>

                <v-card-text class="text--primary">
                  {{ project.description }}
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
      <v-row>
        <v-col>
          <h1 class="thereIsMore">If you want to see more of my projects, just hop on to my GitHub page.</h1>
        </v-col>
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
            "In this project, 5 students and myself, worked in a scrum team to develop a responsive web application." +  
            "I enjoyed the challenge, gained valuable experience, and was able to further develop my skills in Web Development.",
          image:
            "https://github.com/golfbauer/SH-Travel/blob/main/src/frontend/src/assets/images/Luebeck_Login.jpg?raw=true",
        },
        {
          name: "Function Analyzer",
          github:
            "https://github.com/golfbauer/FunctionAnalyzer/tree/main/components/src/main/java/de/hhn/it/pp/components/functionanalyzer",
          description:
            "This beautifull program takes a function as a string and calculates its maxima, minima, intercepts with y and x, etc. " + 
            "It is the result of a one-week work assignment in my third semester. " + 
            "If you dare to look at our code, you can find it if you click on the button below.",
          image:
            "https://github.com/golfbauer/FunctionAnalyzer/blob/main/components/src/main/java/de/hhn/it/pp/components/functionanalyzer/FunctionAnalyzer.png?raw=true",
        },
        {
          name: "Schnek",
          github: "https://github.com/golfbauer/Schnek",
          description:
            "This project is part of a continous assignment for my 2D Game Engine Development module. " + 
            "I just started out with this project and hopefully it will be done by January. " + 
            "The goal is to recreate Snake with some extra features.",
          image:
            "https://github.com/golfbauer/Schnek/blob/main/Games/Schnek/assets/images/SnakeByGoogle.png?raw=true",
        },
        {
          name: "Portfolio",
          github: "https://github.com/golfbauer/MyPortfolio",
          description:
            "Even though you are already on this website I wanted to show that I did not just copy a portfolio from Github. " + 
            "I also used Gridsome and Vuetify to create this Portfolio for the first time, to show my adaptibility.",
          image:
            "https://github.com/golfbauer/MyPortfolio/blob/master/src/profile.jpg?raw=true",
        },
      ],
    };
  },
  methods: {
  
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
.thereIsMore {
  text-align: center;
  font-size: 20px;
}
</style>