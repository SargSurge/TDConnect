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
    <v-dialog v-model="popupOpen">
      <v-card style="margin:10px; padding:20px" width="225" height="350">
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