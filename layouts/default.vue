<template>
  <v-app>
    <v-main>
      <Navbar/>
      <div id="router_view">
        <Nuxt />
      </div>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout'
}
</script>
