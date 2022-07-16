<template>
<v-col align="center">
  <v-layout column wrap align-center>
      <v-flex style="width:100%" v-for="event in events" v-bind:key="event.name">
          <RushCard v-bind:event = "event" />
      </v-flex>
  </v-layout>
</v-col>
</template>

<script>
import RushCard from './RushCard.vue';

export default {
  name: 'RushList',
  components: {RushCard},
  props: ['events'],
  data() {
      return {

      };
  },
}
</script>