<template>
  <div>
    <v-btn
      v-for="(item, i) in items.slice(0, large ? items.length : 3)"
      :key="i"
      fab
      class="ma-2"
      :large="large"
      color="info"
      :href="item.url"
      target="_blank"
    >
      <v-icon
        dark
        v-text="item.icon"
      />
    </v-btn>
  </div>
</template>

<script>
export default {
  props: {
    large: {
      type: Boolean,
      default: false
    }
  },

  data: () => ({
    items: [
      {
        name: 'Github',
        icon: 'mdi-github-circle',
        url: 'https://github.com/kcontreras01'
      },
      {
        name: 'Twitter',
        icon: 'mdi-twitter',
        url: 'https://twitter.com/kiarathedev'
      },
      {
        name: 'Instagram',
        icon: 'mdi-instagram',
        url: 'https://www.instagram.com/kiarathedev/'
      },
      {
        name: 'Linkedin',
        icon: 'mdi-linkedin',
        url: 'https://www.linkedin.com/in/kiaracontreras/'
      },
      {
        name: 'Email',
        icon: 'mdi-email',
        url: 'mailto:kiara.p.contreras@gmail.com'
      }
    ]
  })
}
</script>
