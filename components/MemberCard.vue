<template>
  <div>
    <v-card 
      style="margin:10px; padding:20px" 
      width="225" 
      height="350"
      @click.stop="popupOpen = true"
    >
        <nuxt-img height="200" width="175" :src="member.img" />
        <h2>{{member.name}}</h2>
        <h4>{{member.hometown}}</h4>
        <h4>{{member.course}}</h4>
        <p>{{member.bio}}</p>
    </v-card>
    <v-dialog v-model="popupOpen" max-width="700">
      <v-card style="padding:20px" width="100%" height="400">
          <nuxt-img height="200" width="175" :src="member.img" />
          <h2>{{member.name}}</h2>
          <h4>{{member.hometown}}</h4>
          <h4>{{member.course}}</h4>
          <p>{{member.bio}}</p>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>

export default {
  name: 'MemberCard',
  props: ['member'],
  data() {
      return {
        popupOpen: false,
      };
  },
}
</script>