<template>
  <section
    id="recent-projects"
    class="hide-overflow"
  >
    <v-layout>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/annie-spratt-42051-unsplash.jpg')"
          height="100%"
        />
      </v-flex>
      
      <v-flex
        xs12
        md6
        primary
        text-xs-center
        pa-5
        white--text
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateX(25%); visibility: hidden;"
        />
        <base-heading>
          Projects
        </base-heading>

        <base-text class="mb-5" style="visibility: hidden">
          Lorem ipsum dolor sit amet, consectetur adipi<br>
          scin elit. Etiam vulputate augue vel felis gravida<br>
          porta. Lorem ipsum dolor sit amet.
        </base-text>

        <v-card color="secondary">
          <v-container
            grid-list-md
            pa-2
          >
            <v-layout wrap>
              <v-flex
                v-for="(project, index) in projects"
                :key="index"
                xs12
                md6
              >
                <a :href="`${project.url}`">
                  <v-img
                    :src="require(`@/assets/${project.img}.jpeg`)"
                    max-height="300"
                  />
                </a>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    projects: [
      {img: 'project1', url: ''},
      {img: 'project2', url: ''},
      {img: 'project3', url: ''},
      {img: 'project4', url: ''}
    ]
  })
}
</script>
