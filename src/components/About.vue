<template>
  <section id="about">
    <v-container>
      <v-row class="justify-space-around">
        <v-col>
          <center><g-image alt="Profile image" src="~/profile.jpg"  /></center>
        </v-col>
        <v-col class="d-flex flex-column justify-center">
          <div class="introduction">
            <h1>Hi, I'm Henri.</h1>
            <blockquote>
              <p>
                I am a Software Engineer student with extensive skills in Java
                and responsive Web Applications development.
              </p>
              <p>
                I am currently doing an Erasmus semester at the Dundalk
                Institute of Technology in Ireland.
              </p>
              <p>There I study Games Development as my major field of study.</p>
              <p>
                Next semester, I will be doing an internship, which I would like to do abroad as well.
              </p>
            </blockquote>
            <br />
            <p>
              LinkedIn:
              <a href="https://www.linkedin.com/in/henri-truetsch-16a367222/">
                Henri Truetsch</a
              >
            </p>
            <p>GitHub: <a href="https://github.com/golfbauer"> Golfbauer</a></p>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
.g-image {
  border-radius: 50%;
  max-width: 400px;

}
.introduction h1 {
  margin-bottom: 15px;
  font-size: 30px;
}
.introduction p {
  display: block;
}
</style>