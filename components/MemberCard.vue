<template>
  <div>
    <v-hover
      v-slot="{ hover }"
    >
      <v-card 
        :elevation="hover ? 16 : 2"
        :class="{ 'on-hover': hover }"
        style="margin:10px; padding:20px" 
        width="350" 
        height="450"
        @click.stop="popupOpen = true"
      >
          <nuxt-img height="325" width="275" :src="'/img' + member.img" />
          <h2>{{member.name}}</h2>
          <h4>{{member.hometown}}</h4>
          <h4>{{member.course}}</h4>
          <!-- <p>{{member.bio}}</p> -->
      </v-card>
    </v-hover>
    <v-dialog v-model="popupOpen" max-width="700">
      <v-card style="padding:20px" width="100%">
        <v-row>
          <v-col cols="12" sm="12" md="6"  class="text-center">
            <nuxt-img height="250" width="200" :src="'/img' + member.img" />
          </v-col>
          <v-col col="12" sm="12" md="6" style="margin:auto" class="text-center">
            <h2>{{member.name}}</h2>
            <h4>{{member.hometown}}</h4>
            <h4>{{member.course}}</h4>
            <v-spacer />
            <iframe :src='spotifySrc' style="margin-top:30px" width="300" height="80" frameborder="0" allowtransparency="true" allow="encrypted-media"></iframe>
          </v-col>
        </v-row>
        <v-row>
          <v-card-text>
            <p>{{member.bio}}</p>
          </v-card-text>
        </v-row>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>

export default {
  name: 'MemberCard',
  props: ['member'],
  computed: {
    spotifySrc() {
      return 'https://open.spotify.com/embed/track/' + this.member.song.slice(31, 53);
    }
  },
  data() {
      return {
        popupOpen: false,
      };
  },
}
</script>