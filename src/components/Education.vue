<template>
  <section id="education-experience">
    <v-container>
      <v-row>
        <v-col>
          <h1 style="font-size: 30px;">Education & Experience</h1>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-timeline reverse>
            <v-timeline-item
              v-for="(year, i) in years"
              :key="i"
              :color="year.color"
              small
            >
              <template v-slot:opposite>
                <span
                  :class="`headline font-weight-bold ${year.color}--text`"
                  v-text="year.year"
                ></span>
              </template>
              <div class="py-4">
                <h2
                  :class="`headline font-weight-light mb-4 ${year.color}--text`"
                >
                  {{year.name}}
                </h2>
                <div>
                  <p>{{year.study}}</p>
                  <p>{{year.major}}</p>
                  <p>{{year.semester}}</p>
                  <blockquote>
                  <p>{{year.work}}</p>
                  </blockquote>
                </div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
    data: () => ({
      years: [
        {
          color: 'cyan',
          year: '09/2021 - 01/2022',
          name: 'Dundalk Institute of Technology',
          study: 'Computing in Games Development',
          semester: 'Erasmus Semester',
          work: 'Relevant coursework: 2D and 3D Character Animation, 2D Game Engine Development, Games Physics, Software Testing, Database Systems 2'
        },
        {
          color: 'green',
          year: '09/2019 - 08/2023',
          name: 'Heilbronn University of Applied Sciences',
          study: 'Software Engineering',
          major: 'Major field of study Games Development',
          semester: 'Semester 5',
          work: 'Relevant coursework: Web Development, Software Engineering of Complex Systems, DevOps, Complex Programs, Software Project & Skills Lab'
        },
        {
          color: 'pink',
          year: '2018/09 - 2019/03',
          name: 'Bundeswehr',
          study: 'Wehrdienst [Voluntary Military Service]',
          major: 'Obergefreiter [Corporal]',
          semester: 'Grundausbildung [Basic Training] in Schwarzenborn',
          work: 'Prepared soldiers and civilian employees of various organizations for foreign missions as an auxiliary instructor in Hammelburg.'
        },
        {
          color: 'amber',
          year: '08/2010 - 06/2018',
          name: 'Eltville Gymnasium',
          study: 'Abitur [Highschool]',
        }
      ],
    }),
  }
</script>

