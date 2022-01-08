<template>
    <v-parallax
      dark
      src="https://drive.google.com/uc?export=view&id=1-ZmlogsAQ0JfUzTaF0gk1vbpnr8DBhSB"
      height="800"
    >
      <v-row justify="center" align="center">
        <v-col class="text-center" cols="12" sm="8" md="6">
          <v-overlay opacity=".05" absolute>
            <nuxt-img 
              height="200px"
              src='/tdc-big.png'
            />
            <h1>Welcome to TDC</h1>
          </v-overlay>
        </v-col>
      </v-row>
    </v-parallax>

    <!-- <v-container>
      <v-row justify="center" align="center">
        <v-col class="text-center" cols="12" sm="8" md="6">
          <h1>About Us</h1>
        </v-col>
      </v-row>
    </v-container> -->

</template>

<script>
export default {
  name: 'IndexPage'
}
</script>