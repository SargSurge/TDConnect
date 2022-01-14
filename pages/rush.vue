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
                <h1>Welcome to our community!</h1>
            </div>  
          </v-overlay>
        </v-col>
      </v-row>
    </v-parallax>
  <v-container style="padding-top:50px; padding-bottom:50px;">
    <v-row>
      <v-col class="text-center">
        <h2>We’re Theta Delta Chi, but people usually call us TDC.</h2>
        <h2>Here at TDC we value camaraderie, inclusion, and autonomy.</h2>
        <h2>Peace. Love. Mutual Aid.</h2>  
        <iframe style="margin-top:50px;margin-bottom:50px" width="90%" height="400" src="https://www.youtube-nocookie.com/embed/w0r-SrCv8fA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>        
        <h1>Rush Schedule</h1>
        <h1>Coming Soon!</h1>
        <!-- <v-sheet style="margin-top:40px" height="500">
            <v-calendar
            ref="calendar"
            :now="today"
            :value="today"
            :events="events"
            color="primary"
            type="week"
            ></v-calendar>
        </v-sheet> -->
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
        today: '2019-01-08',
        events: [
            {
            name: 'Weekly Meeting',
            start: '2019-01-07 09:00',
            end: '2019-01-07 10:00',
            },
            {
            name: `Thomas' Birthday`,
            start: '2019-01-10',
            },
            {
            name: 'Mash Potatoes',
            start: '2019-01-09 12:30',
            end: '2019-01-09 15:30',
            },
        ],
    };
  },
  mounted () {
      //this.$refs.calendar.scrollToTime('08:00');
  },
}
</script>