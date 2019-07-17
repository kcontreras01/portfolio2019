<template>
  <div>
    <welcome />
    <about-me />
    <!-- <recent-projects /> -->
  </div>
</template>

<script>
export default {
  components: {
    AboutMe: () => import('@/components/AboutMe'),
    // RecentProjects: () => import('@/components/RecentProjects'),
    Welcome: () => import('@/components/Welcome')
  }
}
</script>
