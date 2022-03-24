<template>
  <div>
    <v-parallax
      style="margin-top:40px"
      dark
      src="https://drive.google.com/uc?export=view&id=1Me_Cb8zLa0ri9K7liHOlZk-rw4xL0Xr-"
      height="600"
    >

      <v-row justify="center" align="center">
        <v-overlay opacity=".1" absolute>
          <v-col cols="12" class="text-center">
            <h1>Welcome To</h1>
            <nuxt-img 
              height="200px"
              src='/img/tdc-big.png'
            />
          </v-col>
          <v-col class="text-center" cols="12">
            <NuxtLink to="/members">
              <v-btn           
                elevation="1"
                outlined 
                x-large
                style="width:150px"
              >
                Members ->
              </v-btn>
            </NuxtLink>
            <NuxtLink to="/rush">
              <v-btn           
                elevation="1"
                outlined 
                x-large
                style="width:150px"
              >
                Rush ->
              </v-btn>
            </NuxtLink>
          </v-col>
        </v-overlay>
      </v-row>
    </v-parallax>
    
    <v-container style="padding-top:30px; padding-bottom:50px">
      <v-row align="center">
        <v-col>
          <h1 style="margin:30px" class="text-center">About Us</h1>
          <p style="margin:10px">Theta Delta Chi boasts a tight-knit group of 30+ active members from a variety of different backgrounds. Members have attended public, private, and boarding schools as well as being home-schooled. They hail from all areas of the United States as well as internationally from Latin America, the Caribbean, and Europe. Their broad backgrounds are exemplified by the fact that members major in almost every engineering major at MIT as well as non-engineering majors and/or minors in fields such as music, biology, management, economics, and brain and cognitive sciences. Member involvement extends throughout the MIT campus. Current members are on the executive boards of DanceTroupe, Live Music Connection, Dramashop, Colleges Against Cancer, the Society of Hispanic Professional Engineers, and the Interfraternity Council. Member involvement on campus extends into student government, intramural sports, academic groups, and community service. Recent graduates have gone into Master's and Doctoral programs at schools including MIT, Yale, and University of Michigan. Others have gone directly into technical fields either nearby in Boston or exploring the world at companies such as Meta, Apple, Amazon, Microsoft, Google, Tesla, and more. Many alumni create start-ups with other Theta Delta Chi brothers and provide internships and career support for active brothers.</p>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
