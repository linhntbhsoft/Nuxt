<template>
  <div>
    <div class="header" style="position:absolute">
      <NavBar />
    </div>
    <Nuxt />
  </div>
</template>

<script>
import NavBar from '~/components/NavBar'
export default {
  components: {
    NavBar
  }
}
</script>

