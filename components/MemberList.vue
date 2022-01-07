<template>
  <v-layout row wrap>
      <v-flex v-for="member in members" v-bind:key="member.name">
          <MemberCard v-bind:member = "member" />
      </v-flex>
  </v-layout>
</template>

<script>
import MemberCard from './MemberCard.vue';

export default {
  name: 'MemberList',
  components: [MemberCard],
  props: ['members'],
  data() {
      return {

      };
  },
}
</script>