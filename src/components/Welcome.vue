<template>
  <section id="welcome" class="hide-overflow">
    <v-layout>
      <v-flex hidden-sm-and-down md6>
        <v-img
          :src="require('@/assets/ren-ran-232079-unsplash.jpg')"
          height="100vh"
        />
      </v-flex>

      <v-flex
        xs12
        md6
        layout
        :pa-5="$vuetify.breakpoint.smAndDown"
        wrap
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateY(25%); visibility: hidden;"
        />

        <v-layout align-center :justify-center="$vuetify.breakpoint.mdAndUp">
          <v-flex xs10 md6>
            <base-heading>Kiara Contreras</base-heading>
            <base-subheading>Full Stack Web Developer</base-subheading>

            <base-text>
              Plant Mom / Cat Lover / Green Tea Junkie
            </base-text>
          </v-flex>
        </v-layout>

        <base-bubble-2
          style="transform: rotate(180deg) translate(-200px, -15%); visibility: hidden;"
        />
      </v-flex>
    </v-layout>
  </section>
</template>
