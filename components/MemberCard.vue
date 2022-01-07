<template>
  <v-card style="margin:10px;" max-width="225" max-height="350">
      <nuxt-img height="200" width="175" :src="member.img" />
      <h2>{{member.name}}</h2>
      <h4>{{member.hometown}}</h4>
      <h4>{{member.course}}</h4>
      <p>{{member.bio}}</p>
  </v-card>
</template>

<script>
export default {
  name: 'MemberCard',
  props: ['member'],
  data() {
      return {

      };
  },
}
</script>