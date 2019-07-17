<template>
  <section id="about" class="hide-overflow">
    <v-layout white>
      <v-flex xs12 md6 pa-5>
        <base-bubble-1
          style="transform: translate(5%, -5%); visibility: hidden;"
        />
        <base-heading class="info--text">
          About Me
        </base-heading>

        <base-text class="mb-5">
          I’m intrigued by improving and crafting digital experiences. With the
          left <br />side of my brain fueled by music and teaching yoga I have
          found that Web <br />Development requires my perceptive nature,
          logical thinking, and resilience.
        </base-text>

        <div class="mb-5">
          <base-subheading class="info--text">
            Skills
          </base-subheading>

          <v-btn v-for="(skill, i) in skills" :key="i" text class="ma-2 info">
            <v-icon dark v-text="skill.icon" />

            <span style="color: white" class="ma-1">
              {{ skill.name }}
            </span>
          </v-btn>
        </div>

        <base-subheading class="info--text">
          Article Posts
        </base-subheading>

        <v-card v-for="article in allArticles" class="ma-2 info" width="75%">
          <a :href="article.url" target="_blank" style="text-decoration: none; color: white">
            <v-card-title primary-title class="headline">
              <v-icon dark class="mr-4">mdi-forum</v-icon>
                {{article.title}}
            </v-card-title>
          </a>
        </v-card>

      </v-flex>
      <v-flex hidden-sm-and-down md6>
        <v-img
          :src="require('@/assets/scott-webb-199479-unsplash.jpg')"
          height="100%"
        />
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
import axios from 'axios'

export default {
  data: () => ({
    skills: [
      { name: "PHP", icon: "mdi-language-php"},
      { name: "Laravel", icon: "mdi-laravel"},
      { name: "VueJS", icon: "mdi-vuejs"},
      { name: "HTML", icon: "mdi-language-html5"},
      { name: "CSS",icon: "mdi-language-css3"},
      { name: "React", icon: "mdi-react"},
      { name: "React Native", icon: "mdi-react"},
      { name: "NodeJS", icon: "mdi-nodejs"},
      { name: "Express", icon: ""},
      { name: "MySQL", icon: ""},
      { name: "PSQL", icon: ""},
    ],
    allArticles: null,
  }),

  mounted () {
    axios
      .get('https://dev.to/api/articles?username=kiarathedev')
      .then(response => (this.allArticles = response.data))
  }
};
</script>
