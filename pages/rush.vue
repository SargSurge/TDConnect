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
    <v-col>
  <div class="d-flex justify-space-between flex-wrap">
        <div style="max-width:700px; margin-bottom:15px">
          <h2>Welcome to TDC!</h2>
          <p>We’re Theta Delta Chi, a Gender-Inclusive Fraternity.</p>
          <p>We allow members to build and paint within the walls of our house (and courtyard) and have a fully equipped makerspace for them to make their ideas a reality. Members of TDC actually designed and built our entire fourth floor!</p>
          <p>We can be found talking, studying, and snacking at all times throughout the day in the House. We love to ideate together, boost each others’ ideas and entrepreneurial pursuits, and support each others’ professional development. We also inspire each other to lead within our communities, whether that be at MIT, Boston, or beyond.</p>
          <p>Join us at TDC! Impromptu adventures! Hiking! Exploring! Dreaming! Discourse! A place for everyone! Introvert or extrovert. We want you here to experience life with us! You can find us at the house after Baker with the owl or the purple light. Our doors are open and we’re excited to meet you!</p>  
        </div>
        <div>
          <iframe style="min-width:400px" height="400" src="https://www.youtube-nocookie.com/embed/w0r-SrCv8fA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>        
        </div>
  </div>
</v-col>
    <!-- <v-row>
      <v-col>
        <h2>Welcome to TDC!</h2>
        <p>We’re Theta Delta Chi, a Gender-Inclusive Fraternity.</p>
        <p>We allow members to build and paint within the walls of our house (and courtyard) and have a fully equipped makerspace for them to make their ideas a reality. Members of TDC actually designed and built our entire fourth floor!</p>
        <p>We can be found talking, studying, and snacking at all times throughout the day in the House. We love to ideate together, boost each others’ ideas and entrepreneurial pursuits, and support each others’ professional development. We also inspire each other to lead within our communities, whether that be at MIT, Boston, or beyond.</p>
        <p>Join us at TDC! Impromptu adventures! Hiking! Exploring! Dreaming! Discourse! A place for everyone! Introvert or extrovert. We want you here to experience life with us! You can find us at the house after Baker with the owl or the purple light. Our doors are open and we’re excited to meet you!</p>  
      </v-col>
      <v-col>
        <iframe style="margin-left:15px" width="90%" height="400" src="https://www.youtube-nocookie.com/embed/w0r-SrCv8fA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>        
        <!-- <h1>Fall 2022 Rush Events</h1> -->
        <!-- <RushList :events="events"/> -->
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
      <!-- </v-col>
    </v-row> --> 
  </v-container>
</div>
</template>

<script>
// import RushList from "../components/RushList.vue";

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