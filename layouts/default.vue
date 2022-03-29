<template>
  <div>
      <Head/>
      <Nuxt/>
      <Foot/>
  </div>
</template>

<script>
import Head from "../components/Header.vue" 
import Foot from "../components/Footer.vue"
export default {
    components: {
        Head,
        Foot,
    } 
}
</script>

<style>

</style>