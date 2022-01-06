<template>
  <v-row justify="center" align="center">
    <v-col class="text-center" cols="12" sm="8" md="6">
      <!-- <v-card class="logo py-4 d-flex justify-center">
        <NuxtLogo />
        <VuetifyLogo />
      </v-card> -->
      <nuxt-img 
        height="200px"
        src='/tdc-big.png'
      />
      <h1>Welcome to TDC</h1>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
