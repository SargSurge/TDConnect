<template>
<div>
<v-parallax
      dark
      src="https://drive.google.com/uc?export=view&id=1hiA1HbYy-GPr0lJny5D2vpDnirJ6c62b"
      height="400"
    >
      <v-row justify="center" align="center">
        <v-col class="text-center" cols="12" sm="8" md="6">
          <v-overlay opacity=".5" absolute>
            <div style="margin-top:100px; margin-bottom:50px">
                <h1>Fall Housing</h1>
            </div>  
          </v-overlay>
        </v-col>
      </v-row>
    </v-parallax>
  <v-container style="padding-top:50px; padding-bottom:50px;">
    <v-row>
      <v-col>
          <div style="padding-bottom:30px;">
            <h1>OPEN TO APPLICATIONS FOR FALL 2022</h1>
            <!-- <h3>Memorable summers with memorable people</h3> -->
          </div>
        <h3>Theta Delta Chi is located on MIT's campus, at 372 Memorial Drive alongside the Charles River.</h3> 
        <h3 style="padding-bottom:10px;">TDC is a great place to live for a multitude of reasons:</h3>  
        <ul>
            <li><b>Location</b> - TDC is the closest fraternity to MIT campus, so you can sleep in a little more and get to lab or the 1 bus faster.</li>
            <li><b>House culture</b> - Our members are quite eclectic and unique. Whether you like to jam with others, paint murals, watch movies, or talk about physics and philosophy, you'll find someone to hang out with.</li>
            <li><b>Safety</b> - MIT campus is monitored by MIT Police 24/7, so you can ensure peace of mind with us.</li>
            <li><b>Roofdecks</b> - We have three roofdecks and a balcony facing the river that allow for beautiful breezes and relaxation.</li>
        </ul>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <div>
            <h2>Pricing</h2>
            <p>Our housing prices make living at Theta Delta Chi one of the most affordable living situations possible. <br> Rooms are available in a fall semester + IAP package from Septmeber 2nd to January 29th. <br> All prices reflect the full semester + IAP package.</p>
        </div>
        <ul>
            <li><b>Single</b> - $5100</li>
            <li><b>Double</b> - $4700</li>
            <li><b>Triple</b> - $4300</li>
        </ul>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <div>
            <h2>Application Timeline</h2>
        </div>
        <ol>
            <li>You apply by filling out our google form!</li>
            <li>We are reviewing applications on a rolling basis, if you are approved we will reach out to you with much more information. You'll also receive a leasing agreement and a request for a security deposit of $500.</li>
            <li>After receiving the leasing agreement, you'll have a week to return a signed agreement and pay the deposit. After that week, we won't hold your spot, so there is no guarantee that there is still space.</li>
            <li>Once everything is submitted, you're all set until you move in! Your full rent will be due on the first day of our move-in period, September 2nd at 11:59pm.</li>
        </ol>
      </v-col>
    </v-row>
    <v-row>
        <v-col>
            <a :href="applyLink"><v-btn color="primary" x-large>Apply Now!</v-btn></a>
        </v-col>
    </v-row>
    
  </v-container>
</div>
</template>

<script>
export default {
  name: 'RushPage',
  components: {},
  computed: {},
  data () {
    return {
        applyLink: "https://forms.gle/X523Tp52ANmxYvfA9",
    };
  },
  mounted () {
      //this.$refs.calendar.scrollToTime('08:00');
  },
}
</script>