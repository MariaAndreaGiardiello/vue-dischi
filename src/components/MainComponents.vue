<template>
  <main>
      <section-cds/>
  </main>
</template>

<script>
import SectionCds from '../components/sections/SectionCds.vue'

export default {
    name : 'MainComponents',
    components: { 
        SectionCds 
    },
}
</script>

<style lang="scss" scoped>
main {
    background-color: var(--secondary-color);
    height: 100vh;
}
</style>